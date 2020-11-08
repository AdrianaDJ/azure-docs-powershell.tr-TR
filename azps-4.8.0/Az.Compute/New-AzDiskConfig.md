---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 4e2e09597cc52431657001e20ca34ad6e77aa40f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268582"
---
# <span data-ttu-id="6ed41-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="6ed41-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="6ed41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ed41-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed41-103">Yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ed41-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="6ed41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ed41-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ed41-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ed41-105">DESCRIPTION</span></span>
<span data-ttu-id="6ed41-106">**New-AzDiskConfig** cmdlet 'i yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ed41-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="6ed41-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ed41-107">EXAMPLES</span></span>

### <span data-ttu-id="6ed41-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ed41-108">Example 1</span></span>
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

<span data-ttu-id="6ed41-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ed41-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="6ed41-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="6ed41-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="6ed41-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ed41-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="6ed41-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ed41-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6ed41-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6ed41-113">Example 2</span></span>
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

<span data-ttu-id="6ed41-114">İlk komut, karşıya yüklemek için yerel bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ed41-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="6ed41-115">İkinci komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ed41-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="6ed41-116">Üçüncü komut, diskin SAS URL 'Sini alır.</span><span class="sxs-lookup"><span data-stu-id="6ed41-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="6ed41-117">Dördüncü komut diskin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="6ed41-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="6ed41-118">Disk durumu ' ReadyToUpload ' ise, Kullanıcı, AzCopy kullanarak bir diski BLOB depolama biriminden disk SAS URL 'sine yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="6ed41-119">Karşıya yükleme sırasında disk durumu ' ActiveUpload ' olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="6ed41-120">Son komut SAS URL 'Si için disk erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="6ed41-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="6ed41-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6ed41-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="6ed41-122">Paylaşılan Galeri görüntüsü sürümünden bir disk oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6ed41-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="6ed41-123">ID, paylaşılan Galeri görüntüsü sürümünün kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="6ed41-124">LUN yalnızca kaynak bir veri diskine ait olduğunda gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="6ed41-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ed41-125">PARAMETERS</span></span>

### <span data-ttu-id="6ed41-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="6ed41-126">-CreateOption</span></span>
<span data-ttu-id="6ed41-127">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="6ed41-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed41-128">-DefaultProfile</span></span>
<span data-ttu-id="6ed41-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ed41-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ed41-130">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6ed41-130">-DiskEncryptionKey</span></span>
<span data-ttu-id="6ed41-131">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-131">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="6ed41-132">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="6ed41-132">-DiskEncryptionSetId</span></span>
<span data-ttu-id="6ed41-133">Rest 'de şifrelemeyi etkinleştirmek için kullanılacak disk şifrelemesi kümesi kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-133">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="6ed41-134">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="6ed41-134">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="6ed41-135">Tüm VM 'lerde izin verilecek toplam ıOPS sayısı, paylaşılan diski salt okunur olarak bağlama.</span><span class="sxs-lookup"><span data-stu-id="6ed41-135">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="6ed41-136">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-136">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="6ed41-137">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ed41-137">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="6ed41-138">Bu diskte izin verilen ıOPS sayısı; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-138">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="6ed41-139">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-139">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="6ed41-140">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="6ed41-140">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="6ed41-141">"Açıklama": tüm VM 'lerde izin verilen toplam üretilen iş (MBps) paylaşılan diski ReadOnly olarak bağlama.</span><span class="sxs-lookup"><span data-stu-id="6ed41-141">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="6ed41-142">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6ed41-142">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="6ed41-143">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="6ed41-143">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="6ed41-144">Bu diskte izin verilen bant genişliği; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-144">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="6ed41-145">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6ed41-145">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="6ed41-146">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6ed41-146">-DiskSizeGB</span></span>
<span data-ttu-id="6ed41-147">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-147">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6ed41-148">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="6ed41-148">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="6ed41-149">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6ed41-149">Enable encryption settings.</span></span>

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

### <span data-ttu-id="6ed41-150">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="6ed41-150">-DiskAccessId</span></span>
<span data-ttu-id="6ed41-151">Özel uç noktaları kullanmak için DiskAccess kaynağının ARM KIMLIĞINI alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ed41-151">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="6ed41-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ed41-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="6ed41-153">Ağ erişimi ilkesi, ağ erişim ilkesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6ed41-153">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="6ed41-154">Olası değerler: ' AllowAll ', ' AllowPrivate ', ' DenyAll '</span><span class="sxs-lookup"><span data-stu-id="6ed41-154">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="6ed41-155">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="6ed41-155">-EncryptionType</span></span>
<span data-ttu-id="6ed41-156">Diskin verilerini şifrelemek için kullanılan anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="6ed41-156">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="6ed41-157">Kullanılabilir değerler şunlardır: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="6ed41-157">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="6ed41-158">-Gallerimagereference</span><span class="sxs-lookup"><span data-stu-id="6ed41-158">-GalleryImageReference</span></span>
<span data-ttu-id="6ed41-159">Gallerimagereference nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6ed41-159">The GalleryImageReference object.</span></span>  <span data-ttu-id="6ed41-160">Galeri görüntüsünden oluşturma için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-160">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="6ed41-161">Kimlik, diskin oluşturulacağı paylaşılan Gale görüntü sürümünün ARM kimliği olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6ed41-161">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="6ed41-162">Kopyanın kaynağı Galeri görüntüsündeki veri disklerinden biri ise bir LUN gereklidir; null ise, yansımanın işletim sistemi diski kopyalanacaktır.</span><span class="sxs-lookup"><span data-stu-id="6ed41-162">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="6ed41-163">-Hiper VCR</span><span class="sxs-lookup"><span data-stu-id="6ed41-163">-HyperVGeneration</span></span>
<span data-ttu-id="6ed41-164">Sanal makinenin Hiper Yöneticisi üretimi.</span><span class="sxs-lookup"><span data-stu-id="6ed41-164">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="6ed41-165">Yalnızca işletim sistemi disklerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-165">Applicable to OS disks only.</span></span>  <span data-ttu-id="6ed41-166">İzin verilen değerler v1 ve v2.</span><span class="sxs-lookup"><span data-stu-id="6ed41-166">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="6ed41-167">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="6ed41-167">-ImageReference</span></span>
<span data-ttu-id="6ed41-168">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-168">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="6ed41-169">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6ed41-169">-KeyEncryptionKey</span></span>
<span data-ttu-id="6ed41-170">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-170">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="6ed41-171">-Konum</span><span class="sxs-lookup"><span data-stu-id="6ed41-171">-Location</span></span>
<span data-ttu-id="6ed41-172">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-172">Specifies a location.</span></span>

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

### <span data-ttu-id="6ed41-173">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="6ed41-173">-MaxSharesCount</span></span>
<span data-ttu-id="6ed41-174">Diske aynı anda iliştirileceği en fazla VM sayısı.</span><span class="sxs-lookup"><span data-stu-id="6ed41-174">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="6ed41-175">Birden büyük değer aynı anda birden fazla VM 'ye takılacak bir diski belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-175">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="6ed41-176">-OsType</span><span class="sxs-lookup"><span data-stu-id="6ed41-176">-OsType</span></span>
<span data-ttu-id="6ed41-177">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-177">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6ed41-178">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6ed41-178">-SkuName</span></span>
<span data-ttu-id="6ed41-179">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-179">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="6ed41-180">Kullanılabilir değerler Standard_LRS, Premium_LRS, StandardSSD_LRS ve UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="6ed41-180">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="6ed41-181">UltraSSD_LRS, Createoptıon parametresinde yalnızca boş değer ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-181">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="6ed41-182">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="6ed41-182">-SourceResourceId</span></span>
<span data-ttu-id="6ed41-183">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-183">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="6ed41-184">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="6ed41-184">-SourceUri</span></span>
<span data-ttu-id="6ed41-185">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-185">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="6ed41-186">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="6ed41-186">-StorageAccountId</span></span>
<span data-ttu-id="6ed41-187">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-187">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="6ed41-188">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6ed41-188">-Tag</span></span>
<span data-ttu-id="6ed41-189">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6ed41-189">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ed41-190">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="6ed41-190">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6ed41-191">-Uploadsizeınbytes</span><span class="sxs-lookup"><span data-stu-id="6ed41-191">-UploadSizeInBytes</span></span>
<span data-ttu-id="6ed41-192">Createoptıon karşıya yüklendiğinde VHD altbilgisi dahil karşıya yükleme içeriğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-192">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="6ed41-193">Bu değer, 20972032 (VHD alt bilgisinin 20 MIB + 512 baytı) ve 35183298347520 baytı (VHD altbilgisi için 32 TiB + 512 bytes) arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ed41-193">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="6ed41-194">-Bölge</span><span class="sxs-lookup"><span data-stu-id="6ed41-194">-Zone</span></span>
<span data-ttu-id="6ed41-195">Diskin mantıksal bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-195">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="6ed41-196">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ed41-196">-Confirm</span></span>
<span data-ttu-id="6ed41-197">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ed41-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ed41-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ed41-198">-WhatIf</span></span>
<span data-ttu-id="6ed41-199">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ed41-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ed41-200">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ed41-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ed41-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed41-201">CommonParameters</span></span>
<span data-ttu-id="6ed41-202">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ed41-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed41-203">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6ed41-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed41-204">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ed41-204">INPUTS</span></span>

### <span data-ttu-id="6ed41-205">System. String</span><span class="sxs-lookup"><span data-stu-id="6ed41-205">System.String</span></span>

### <span data-ttu-id="6ed41-206">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6ed41-206">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6ed41-207">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6ed41-207">System.Int32</span></span>

### <span data-ttu-id="6ed41-208">System. String []</span><span class="sxs-lookup"><span data-stu-id="6ed41-208">System.String[]</span></span>

### <span data-ttu-id="6ed41-209">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ed41-209">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6ed41-210">Microsoft. Azure. Management. COMPUTE. modeller. ımagediskreference</span><span class="sxs-lookup"><span data-stu-id="6ed41-210">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="6ed41-211">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ed41-211">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6ed41-212">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="6ed41-212">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="6ed41-213">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="6ed41-213">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="6ed41-214">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ed41-214">OUTPUTS</span></span>

### <span data-ttu-id="6ed41-215">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="6ed41-215">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="6ed41-216">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ed41-216">NOTES</span></span>

## <span data-ttu-id="6ed41-217">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ed41-217">RELATED LINKS</span></span>
