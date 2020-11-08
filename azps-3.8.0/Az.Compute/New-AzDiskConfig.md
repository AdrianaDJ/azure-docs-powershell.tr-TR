---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 7a8c4bc3b875cb9072386784fe1c06730be89405
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096952"
---
# <span data-ttu-id="b6ed2-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b6ed2-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="b6ed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ed2-103">Yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="b6ed2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6ed2-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6ed2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6ed2-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ed2-106">**New-AzDiskConfig** cmdlet 'i yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="b6ed2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6ed2-107">EXAMPLES</span></span>

### <span data-ttu-id="b6ed2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b6ed2-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="b6ed2-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="b6ed2-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="b6ed2-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="b6ed2-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b6ed2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b6ed2-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="b6ed2-114">İlk komut, karşıya yüklemek için yerel bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="b6ed2-115">İkinci komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="b6ed2-116">Üçüncü komut, diskin SAS URL 'Sini alır.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="b6ed2-117">Dördüncü komut diskin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="b6ed2-118">Disk durumu ' ReadyToUpload ' ise, Kullanıcı, AzCopy kullanarak bir diski BLOB depolama biriminden disk SAS URL 'sine yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="b6ed2-119">Karşıya yükleme sırasında disk durumu ' ActiveUpload ' olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="b6ed2-120">Son komut SAS URL 'Si için disk erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="b6ed2-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b6ed2-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="b6ed2-122">Paylaşılan Galeri görüntüsü sürümünden bir disk oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="b6ed2-123">ID, paylaşılan Galeri görüntüsü sürümünün kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="b6ed2-124">LUN yalnızca kaynak bir veri diskine ait olduğunda gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="b6ed2-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6ed2-125">PARAMETERS</span></span>

### <span data-ttu-id="b6ed2-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b6ed2-126">-CreateOption</span></span>
<span data-ttu-id="b6ed2-127">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="b6ed2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ed2-128">-DefaultProfile</span></span>
<span data-ttu-id="b6ed2-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6ed2-130">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b6ed2-130">-DiskEncryptionKey</span></span>
<span data-ttu-id="b6ed2-131">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-131">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-132">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b6ed2-132">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b6ed2-133">Rest 'de şifrelemeyi etkinleştirmek için kullanılacak disk şifrelemesi kümesi kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-133">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="b6ed2-134">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="b6ed2-134">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="b6ed2-135">Tüm VM 'lerde izin verilecek toplam ıOPS sayısı, paylaşılan diski salt okunur olarak bağlama.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-135">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="b6ed2-136">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-136">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-137">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="b6ed2-137">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="b6ed2-138">Bu diskte izin verilen ıOPS sayısı; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-138">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="b6ed2-139">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-139">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-140">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="b6ed2-140">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="b6ed2-141">"Açıklama": tüm VM 'lerde izin verilen toplam üretilen iş (MBps) paylaşılan diski ReadOnly olarak bağlama.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-141">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="b6ed2-142">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-142">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-143">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="b6ed2-143">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="b6ed2-144">Bu diskte izin verilen bant genişliği; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-144">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="b6ed2-145">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-145">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-146">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b6ed2-146">-DiskSizeGB</span></span>
<span data-ttu-id="b6ed2-147">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-147">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-148">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="b6ed2-148">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b6ed2-149">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-149">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-150">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="b6ed2-150">-EncryptionType</span></span>
<span data-ttu-id="b6ed2-151">Diskin verilerini şifrelemek için kullanılan anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-151">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="b6ed2-152">Kullanılabilir değerler şunlardır: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="b6ed2-152">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="b6ed2-153">-Gallerimagereference</span><span class="sxs-lookup"><span data-stu-id="b6ed2-153">-GalleryImageReference</span></span>
<span data-ttu-id="b6ed2-154">Gallerimagereference nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-154">The GalleryImageReference object.</span></span>  <span data-ttu-id="b6ed2-155">Galeri görüntüsünden oluşturma için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-155">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="b6ed2-156">Kimlik, diskin oluşturulacağı paylaşılan Gale görüntü sürümünün ARM kimliği olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-156">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="b6ed2-157">Kopyanın kaynağı Galeri görüntüsündeki veri disklerinden biri ise bir LUN gereklidir; null ise, yansımanın işletim sistemi diski kopyalanacaktır.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-157">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-158">-Hiper VCR</span><span class="sxs-lookup"><span data-stu-id="b6ed2-158">-HyperVGeneration</span></span>
<span data-ttu-id="b6ed2-159">Sanal makinenin Hiper Yöneticisi üretimi.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-159">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="b6ed2-160">Yalnızca işletim sistemi disklerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-160">Applicable to OS disks only.</span></span>  <span data-ttu-id="b6ed2-161">İzin verilen değerler v1 ve v2.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-161">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="b6ed2-162">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="b6ed2-162">-ImageReference</span></span>
<span data-ttu-id="b6ed2-163">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-163">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-164">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b6ed2-164">-KeyEncryptionKey</span></span>
<span data-ttu-id="b6ed2-165">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-165">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-166">-Konum</span><span class="sxs-lookup"><span data-stu-id="b6ed2-166">-Location</span></span>
<span data-ttu-id="b6ed2-167">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-167">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-168">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="b6ed2-168">-MaxSharesCount</span></span>
<span data-ttu-id="b6ed2-169">Diske aynı anda iliştirileceği en fazla VM sayısı.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-169">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="b6ed2-170">Birden büyük değer aynı anda birden fazla VM 'ye takılacak bir diski belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-170">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="b6ed2-171">-OsType</span><span class="sxs-lookup"><span data-stu-id="b6ed2-171">-OsType</span></span>
<span data-ttu-id="b6ed2-172">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-172">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b6ed2-173">-SkuName</span></span>
<span data-ttu-id="b6ed2-174">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-174">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="b6ed2-175">Kullanılabilir değerler Standard_LRS, Premium_LRS, StandardSSD_LRS ve UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-175">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="b6ed2-176">UltraSSD_LRS, Createoptıon parametresinde yalnızca boş değer ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-176">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-177">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="b6ed2-177">-SourceResourceId</span></span>
<span data-ttu-id="b6ed2-178">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-178">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="b6ed2-179">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="b6ed2-179">-SourceUri</span></span>
<span data-ttu-id="b6ed2-180">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-180">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="b6ed2-181">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="b6ed2-181">-StorageAccountId</span></span>
<span data-ttu-id="b6ed2-182">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-182">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="b6ed2-183">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b6ed2-183">-Tag</span></span>
<span data-ttu-id="b6ed2-184">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b6ed2-185">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="b6ed2-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-186">-Uploadsizeınbytes</span><span class="sxs-lookup"><span data-stu-id="b6ed2-186">-UploadSizeInBytes</span></span>
<span data-ttu-id="b6ed2-187">Createoptıon karşıya yüklendiğinde VHD altbilgisi dahil karşıya yükleme içeriğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-187">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="b6ed2-188">Bu değer, 20972032 (VHD alt bilgisinin 20 MIB + 512 baytı) ve 35183298347520 baytı (VHD altbilgisi için 32 TiB + 512 bytes) arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-188">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-189">-Bölge</span><span class="sxs-lookup"><span data-stu-id="b6ed2-189">-Zone</span></span>
<span data-ttu-id="b6ed2-190">Diskin mantıksal bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-190">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-191">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6ed2-191">-Confirm</span></span>
<span data-ttu-id="b6ed2-192">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6ed2-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ed2-193">-WhatIf</span></span>
<span data-ttu-id="b6ed2-194">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-194">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6ed2-195">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6ed2-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ed2-196">CommonParameters</span></span>
<span data-ttu-id="b6ed2-197">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ed2-198">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ed2-199">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6ed2-199">INPUTS</span></span>

### <span data-ttu-id="b6ed2-200">System. String</span><span class="sxs-lookup"><span data-stu-id="b6ed2-200">System.String</span></span>

### <span data-ttu-id="b6ed2-201">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b6ed2-201">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b6ed2-202">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b6ed2-202">System.Int32</span></span>

### <span data-ttu-id="b6ed2-203">System. String []</span><span class="sxs-lookup"><span data-stu-id="b6ed2-203">System.String[]</span></span>

### <span data-ttu-id="b6ed2-204">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6ed2-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b6ed2-205">Microsoft. Azure. Management. COMPUTE. modeller. ımagediskreference</span><span class="sxs-lookup"><span data-stu-id="b6ed2-205">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="b6ed2-206">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="b6ed2-206">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b6ed2-207">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="b6ed2-207">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="b6ed2-208">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="b6ed2-208">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="b6ed2-209">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6ed2-209">OUTPUTS</span></span>

### <span data-ttu-id="b6ed2-210">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="b6ed2-210">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="b6ed2-211">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6ed2-211">NOTES</span></span>

## <span data-ttu-id="b6ed2-212">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6ed2-212">RELATED LINKS</span></span>
