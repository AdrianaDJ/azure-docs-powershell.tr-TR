---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 378d0d33d6cc1ceb2eca4773d93f76afbf75cf4b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936826"
---
# <span data-ttu-id="deb9f-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="deb9f-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="deb9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="deb9f-103">Sanal makinedeki işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="deb9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="deb9f-104">SYNTAX</span></span>

### <span data-ttu-id="deb9f-105">DefaultParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="deb9f-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deb9f-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="deb9f-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deb9f-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="deb9f-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="deb9f-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="deb9f-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deb9f-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="deb9f-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="deb9f-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="deb9f-110">DESCRIPTION</span></span>
<span data-ttu-id="deb9f-111">**Set-Azvmosdısk** cmdlet 'i, sanal makinedeki işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="deb9f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="deb9f-112">EXAMPLES</span></span>

### <span data-ttu-id="deb9f-113">Örnek 1: sanal makinedeki özellikleri platform görüntüsünden ayarlama</span><span class="sxs-lookup"><span data-stu-id="deb9f-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="deb9f-114">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet13 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="deb9f-115">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="deb9f-116">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="deb9f-117">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="deb9f-118">Son komutu $VirtualMachine sanal makinesindeki özellikleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="deb9f-119">Örnek 2: Genelleştirilmiş Kullanıcı görüntüsünden sanal makinedeki özellikleri ayarlar</span><span class="sxs-lookup"><span data-stu-id="deb9f-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="deb9f-120">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet13 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="deb9f-121">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="deb9f-122">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="deb9f-123">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="deb9f-124">Son komutu $VirtualMachine sanal makinesindeki özellikleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="deb9f-125">Örnek 3: özelleştirilmiş Kullanıcı görüntüsünden sanal makinedeki özellikleri ayarlar</span><span class="sxs-lookup"><span data-stu-id="deb9f-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="deb9f-126">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet13 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="deb9f-127">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="deb9f-128">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="deb9f-129">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="deb9f-130">Son komutu $VirtualMachine sanal makinesindeki özellikleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="deb9f-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="deb9f-131">Örnek 4: sanal makine işletim sistemi diskinde disk şifrelemesi ayarlarını yapma</span><span class="sxs-lookup"><span data-stu-id="deb9f-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="deb9f-132">Bu örnekte, sanal makine işletim sistemi diskindeki disk şifrelemesi ayarları ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="deb9f-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="deb9f-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="deb9f-133">PARAMETERS</span></span>

### <span data-ttu-id="deb9f-134">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="deb9f-134">-Caching</span></span>
<span data-ttu-id="deb9f-135">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="deb9f-136">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="deb9f-136">Valid values are:</span></span> 

- <span data-ttu-id="deb9f-137">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="deb9f-137">ReadOnly</span></span>
- <span data-ttu-id="deb9f-138">Yazma</span><span class="sxs-lookup"><span data-stu-id="deb9f-138">ReadWrite</span></span>

<span data-ttu-id="deb9f-139">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="deb9f-140">Önbellek değerini değiştirmek sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="deb9f-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="deb9f-141">Bu ayar, diskin performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="deb9f-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="deb9f-142">-CreateOption</span></span>
<span data-ttu-id="deb9f-143">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını veya mevcut bir diski iliştirir belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="deb9f-144">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="deb9f-144">Valid values are:</span></span> 

- <span data-ttu-id="deb9f-145">Nota.</span><span class="sxs-lookup"><span data-stu-id="deb9f-145">Attach.</span></span>
<span data-ttu-id="deb9f-146">Özel bir diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="deb9f-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="deb9f-147">Bu seçeneği belirttiğinizde *Sourceımageuri* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="deb9f-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="deb9f-148">Bunun yerine Set-AzVMSourceImage cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="deb9f-148">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="deb9f-149">Ayrıca, azure2 platformunu VHD 'deki işletim sisteminin türüne bildirmek için *Windows* veya *Linux* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="deb9f-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="deb9f-150">*Vhduri* parametresi, azure2 platformunu eklemek için diskin konumunu anlatabilecek kadar yeterli.</span><span class="sxs-lookup"><span data-stu-id="deb9f-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="deb9f-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="deb9f-151">FromImage.</span></span>
<span data-ttu-id="deb9f-152">Bir platform görüntüsünden veya Genelleştirilmiş Kullanıcı görüntüsünden sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="deb9f-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="deb9f-153">Genelleştirilmiş bir Kullanıcı görüntüsü olması durumunda, ayrıca *Sourceımageuri* parametresini ve *Windows* veya *Linux* parametrelerini belirtmek Için, **set-azvmsourceımage** CMDLET 'ini kullanmak yerine, işletim sistemi disk VHD 'sinin konumunu ve türünü belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="deb9f-154">Platform görüntüsü durumunda, *Vhduri* parametresi yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="deb9f-155">Boşaltma.</span><span class="sxs-lookup"><span data-stu-id="deb9f-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb9f-156">-DefaultProfile</span></span>
<span data-ttu-id="deb9f-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="deb9f-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deb9f-158">-DiskEncryptionKeyUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="deb9f-158">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="deb9f-159">Disk şifrelemesi anahtarının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-159">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-160">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="deb9f-160">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="deb9f-161">Disk şifrelemesi anahtarını içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-161">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="deb9f-162">-DiskSizeInGB</span></span>
<span data-ttu-id="deb9f-163">İşletim sistemi diskinin boyutunu GB cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-163">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-164">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="deb9f-164">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="deb9f-165">Anahtar şifreleme anahtarının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-165">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-166">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="deb9f-166">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="deb9f-167">Anahtar şifreleme anahtarını içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-167">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="deb9f-168">-Linux</span></span>
<span data-ttu-id="deb9f-169">Kullanıcı görüntüsündeki işletim sisteminin Linux olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-169">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="deb9f-170">Kullanıcı görüntüsü tabanlı sanal makine dağıtımı için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="deb9f-170">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-171">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="deb9f-171">-ManagedDiskId</span></span>
<span data-ttu-id="deb9f-172">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-172">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="deb9f-173">-Ad</span><span class="sxs-lookup"><span data-stu-id="deb9f-173">-Name</span></span>
<span data-ttu-id="deb9f-174">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-174">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-175">-Sourceımageuri</span><span class="sxs-lookup"><span data-stu-id="deb9f-175">-SourceImageUri</span></span>
<span data-ttu-id="deb9f-176">Kullanıcı görüntüsü için VHD 'nin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-176">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="deb9f-177">-StorageAccountType</span></span>
<span data-ttu-id="deb9f-178">Yönetilen diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-178">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-179">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="deb9f-179">-VhdUri</span></span>
<span data-ttu-id="deb9f-180">Sanal bir sabit diskin (URI) Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-180">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="deb9f-181">Görüntü tabanlı sanal makine için, bu parametre bir platform görüntüsü veya Kullanıcı görüntüsü belirtildiğinde oluşturulacak VHD dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-181">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="deb9f-182">Bu, sanal makineyi başlatmak için resim ikili büyük nesnesinin (BLOB) kopyalandığı konumdur.</span><span class="sxs-lookup"><span data-stu-id="deb9f-182">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="deb9f-183">Disk tabanlı sanal makine önyükleme senaryosu için, bu parametre sanal makinenin doğrudan başlatılması için kullandığı VHD dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-183">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-184">-VM</span><span class="sxs-lookup"><span data-stu-id="deb9f-184">-VM</span></span>
<span data-ttu-id="deb9f-185">İşletim sistemi disk özelliklerini ayarlanacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-185">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="deb9f-186">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="deb9f-186">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-187">-Windows</span><span class="sxs-lookup"><span data-stu-id="deb9f-187">-Windows</span></span>
<span data-ttu-id="deb9f-188">Kullanıcı yansımasındaki işletim sisteminin Windows olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-188">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deb9f-189">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="deb9f-189">-WriteAccelerator</span></span>
<span data-ttu-id="deb9f-190">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="deb9f-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="deb9f-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb9f-191">CommonParameters</span></span>
<span data-ttu-id="deb9f-192">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="deb9f-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb9f-193">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb9f-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb9f-194">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="deb9f-194">INPUTS</span></span>

### <span data-ttu-id="deb9f-195">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="deb9f-195">PSVirtualMachine</span></span>
<span data-ttu-id="deb9f-196">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="deb9f-196">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="deb9f-197">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="deb9f-197">OUTPUTS</span></span>

### <span data-ttu-id="deb9f-198">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="deb9f-198">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="deb9f-199">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="deb9f-199">NOTES</span></span>

## <span data-ttu-id="deb9f-200">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="deb9f-200">RELATED LINKS</span></span>

[<span data-ttu-id="deb9f-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="deb9f-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="deb9f-202">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="deb9f-202">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="deb9f-203">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="deb9f-203">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


