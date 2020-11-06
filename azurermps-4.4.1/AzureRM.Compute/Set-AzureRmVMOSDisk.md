---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: c8d1f4713f3f6983d846d041896265ed0c33f5ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591792"
---
# <span data-ttu-id="f14c4-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="f14c4-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="f14c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f14c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f14c4-103">Sanal makinedeki işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f14c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f14c4-104">SYNTAX</span></span>

### <span data-ttu-id="f14c4-105">DefaultParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f14c4-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes>
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14c4-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="f14c4-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14c4-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14c4-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14c4-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="f14c4-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14c4-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14c4-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f14c4-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f14c4-110">DESCRIPTION</span></span>
<span data-ttu-id="f14c4-111">**Set-Azurermvmosdısk** cmdlet 'i sanal makinede işletim sistemi disk özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-111">The **Set-AzureRmVMOSDisk** cmdlet set the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="f14c4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f14c4-112">EXAMPLES</span></span>

### <span data-ttu-id="f14c4-113">Örnek 1: sanal makinedeki özellikleri platform görüntüsünden ayarlama</span><span class="sxs-lookup"><span data-stu-id="f14c4-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f14c4-114">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet13 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f14c4-115">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f14c4-116">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f14c4-117">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f14c4-118">Son komutu $VirtualMachine sanal makinesindeki özellikleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f14c4-119">Örnek 2: Genelleştirilmiş Kullanıcı görüntüsünden sanal makinedeki özellikleri ayarlar</span><span class="sxs-lookup"><span data-stu-id="f14c4-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f14c4-120">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet13 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f14c4-121">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f14c4-122">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f14c4-123">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f14c4-124">Son komutu $VirtualMachine sanal makinesindeki özellikleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f14c4-125">Örnek 3: özelleştirilmiş Kullanıcı görüntüsünden sanal makinedeki özellikleri ayarlar</span><span class="sxs-lookup"><span data-stu-id="f14c4-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="f14c4-126">İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet13 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f14c4-127">İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f14c4-128">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f14c4-129">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f14c4-130">Son komutu $VirtualMachine sanal makinesindeki özellikleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f14c4-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="f14c4-131">Örnek 4: sanal makine işletim sistemi diskinde disk şifrelemesi ayarlarını yapma</span><span class="sxs-lookup"><span data-stu-id="f14c4-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="f14c4-132">Bu örnekte, sanal makine işletim sistemi diskindeki disk şifrelemesi ayarları ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="f14c4-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="f14c4-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f14c4-133">PARAMETERS</span></span>

### <span data-ttu-id="f14c4-134">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="f14c4-134">-Caching</span></span>
<span data-ttu-id="f14c4-135">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="f14c4-136">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f14c4-136">Valid values are:</span></span> 

- <span data-ttu-id="f14c4-137">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="f14c4-137">ReadOnly</span></span>
- <span data-ttu-id="f14c4-138">Yazma</span><span class="sxs-lookup"><span data-stu-id="f14c4-138">ReadWrite</span></span>

<span data-ttu-id="f14c4-139">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="f14c4-140">Önbellek değerini değiştirmek sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="f14c4-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="f14c4-141">Bu ayar, diskin performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="f14c4-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f14c4-142">-CreateOption</span></span>
<span data-ttu-id="f14c4-143">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını veya mevcut bir diski iliştirir belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="f14c4-144">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f14c4-144">Valid values are:</span></span> 

- <span data-ttu-id="f14c4-145">Nota.</span><span class="sxs-lookup"><span data-stu-id="f14c4-145">Attach.</span></span>
<span data-ttu-id="f14c4-146">Özel bir diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="f14c4-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="f14c4-147">Bu seçeneği belirttiğinizde *Sourceımageuri* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="f14c4-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="f14c4-148">Bunun yerine Set-AzureRmVMSourceImage cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f14c4-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="f14c4-149">Ayrıca, azure2 platformunu VHD 'deki işletim sisteminin türüne bildirmek için *Windows* veya *Linux* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f14c4-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="f14c4-150">*Vhduri* parametresi, azure2 platformunu eklemek için diskin konumunu anlatabilecek kadar yeterli.</span><span class="sxs-lookup"><span data-stu-id="f14c4-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="f14c4-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="f14c4-151">FromImage.</span></span>
<span data-ttu-id="f14c4-152">Bir platform görüntüsünden veya Genelleştirilmiş Kullanıcı görüntüsünden sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="f14c4-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="f14c4-153">Genelleştirilmiş bir Kullanıcı görüntüsü olması durumunda, *Sourceımageuri* parametresini ve *Windows* veya *Linux* parametrelerini belirtmek Için, **set-azurermvmsourceımage** CMDLET 'ini kullanmak yerine, işletim sistemi disk VHD 'sinin konumunu ve türünü belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="f14c4-154">Platform görüntüsü durumunda, *Vhduri* parametresi yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="f14c4-155">Boşaltma.</span><span class="sxs-lookup"><span data-stu-id="f14c4-155">Empty.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14c4-156">-DefaultProfile</span></span>
<span data-ttu-id="f14c4-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f14c4-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f14c4-158">-DiskEncryptionKeyUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="f14c4-158">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="f14c4-159">Disk şifrelemesi anahtarının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-159">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-160">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f14c4-160">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="f14c4-161">Disk şifrelemesi anahtarını içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-161">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="f14c4-162">-DiskSizeInGB</span></span>
<span data-ttu-id="f14c4-163">İşletim sistemi diskinin boyutunu GB cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-163">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-164">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f14c4-164">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="f14c4-165">Anahtar şifreleme anahtarının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-165">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-166">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f14c4-166">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="f14c4-167">Anahtar şifreleme anahtarını içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-167">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="f14c4-168">-Linux</span></span>
<span data-ttu-id="f14c4-169">Kullanıcı görüntüsündeki işletim sisteminin Linux olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-169">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="f14c4-170">Kullanıcı görüntüsü tabanlı sanal makine dağıtımı için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="f14c4-170">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-171">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="f14c4-171">-ManagedDiskId</span></span>
<span data-ttu-id="f14c4-172">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-172">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="f14c4-173">-Ad</span><span class="sxs-lookup"><span data-stu-id="f14c4-173">-Name</span></span>
<span data-ttu-id="f14c4-174">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-174">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-175">-Sourceımageuri</span><span class="sxs-lookup"><span data-stu-id="f14c4-175">-SourceImageUri</span></span>
<span data-ttu-id="f14c4-176">Kullanıcı görüntüsü için VHD 'nin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-176">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f14c4-177">-StorageAccountType</span></span>
<span data-ttu-id="f14c4-178">Yönetilen diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-178">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-179">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="f14c4-179">-VhdUri</span></span>
<span data-ttu-id="f14c4-180">Sanal bir sabit diskin (URI) Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-180">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="f14c4-181">Görüntü tabanlı sanal makine için, bu parametre bir platform görüntüsü veya Kullanıcı görüntüsü belirtildiğinde oluşturulacak VHD dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-181">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="f14c4-182">Bu, sanal makineyi başlatmak için resim ikili büyük nesnesinin (BLOB) kopyalandığı konumdur.</span><span class="sxs-lookup"><span data-stu-id="f14c4-182">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="f14c4-183">Disk tabanlı sanal makine önyükleme senaryosu için, bu parametre sanal makinenin doğrudan başlatılması için kullandığı VHD dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-183">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-184">-VM</span><span class="sxs-lookup"><span data-stu-id="f14c4-184">-VM</span></span>
<span data-ttu-id="f14c4-185">İşletim sistemi disk özelliklerini ayarlanacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-185">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="f14c4-186">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f14c4-186">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="f14c4-187">-Windows</span><span class="sxs-lookup"><span data-stu-id="f14c4-187">-Windows</span></span>
<span data-ttu-id="f14c4-188">Kullanıcı yansımasındaki işletim sisteminin Windows olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f14c4-188">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14c4-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14c4-189">CommonParameters</span></span>
<span data-ttu-id="f14c4-190">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f14c4-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14c4-191">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f14c4-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14c4-192">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f14c4-192">INPUTS</span></span>

## <span data-ttu-id="f14c4-193">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f14c4-193">OUTPUTS</span></span>

## <span data-ttu-id="f14c4-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f14c4-194">NOTES</span></span>

## <span data-ttu-id="f14c4-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f14c4-195">RELATED LINKS</span></span>

[<span data-ttu-id="f14c4-196">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f14c4-196">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f14c4-197">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f14c4-197">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="f14c4-198">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="f14c4-198">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


