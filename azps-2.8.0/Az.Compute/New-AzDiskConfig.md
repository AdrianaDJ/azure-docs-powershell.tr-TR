---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: c37ed947441789951d8523f38e7950ad6d9d2066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752863"
---
# <span data-ttu-id="1c609-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1c609-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="1c609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c609-102">SYNOPSIS</span></span>
<span data-ttu-id="1c609-103">Yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c609-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="1c609-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c609-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c609-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c609-105">DESCRIPTION</span></span>
<span data-ttu-id="1c609-106">**New-AzDiskConfig** cmdlet 'i yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c609-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="1c609-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c609-107">EXAMPLES</span></span>

### <span data-ttu-id="1c609-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1c609-108">Example 1</span></span>
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

<span data-ttu-id="1c609-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c609-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="1c609-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="1c609-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="1c609-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c609-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="1c609-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c609-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1c609-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1c609-113">Example 2</span></span>
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

<span data-ttu-id="1c609-114">İlk komut, karşıya yüklemek için yerel bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c609-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="1c609-115">İkinci komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c609-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="1c609-116">Üçüncü komut, diskin SAS URL 'Sini alır.</span><span class="sxs-lookup"><span data-stu-id="1c609-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="1c609-117">Dördüncü komut diskin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="1c609-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="1c609-118">Disk durumu ' ReadyToUpload ' ise, Kullanıcı, AzCopy kullanarak bir diski BLOB depolama biriminden disk SAS URL 'sine yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="1c609-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="1c609-119">Karşıya yükleme sırasında disk durumu ' ActiveUpload ' olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="1c609-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="1c609-120">Son komut SAS URL 'Si için disk erişimini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="1c609-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="1c609-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c609-121">PARAMETERS</span></span>

### <span data-ttu-id="1c609-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="1c609-122">-CreateOption</span></span>
<span data-ttu-id="1c609-123">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="1c609-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="1c609-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c609-124">-DefaultProfile</span></span>
<span data-ttu-id="1c609-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c609-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c609-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1c609-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="1c609-127">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="1c609-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="1c609-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="1c609-129">Bu diskte izin verilen ıOPS sayısı; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="1c609-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1c609-130">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="1c609-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="1c609-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="1c609-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="1c609-132">Bu diskte izin verilen bant genişliği; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="1c609-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1c609-133">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1c609-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="1c609-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1c609-134">-DiskSizeGB</span></span>
<span data-ttu-id="1c609-135">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="1c609-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1c609-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="1c609-137">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="1c609-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="1c609-138">-Hiper VCR</span><span class="sxs-lookup"><span data-stu-id="1c609-138">-HyperVGeneration</span></span>
<span data-ttu-id="1c609-139">Sanal makinenin Hiper Yöneticisi üretimi.</span><span class="sxs-lookup"><span data-stu-id="1c609-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="1c609-140">Yalnızca işletim sistemi disklerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="1c609-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="1c609-141">İzin verilen değerler v1 ve v2.</span><span class="sxs-lookup"><span data-stu-id="1c609-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="1c609-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="1c609-142">-ImageReference</span></span>
<span data-ttu-id="1c609-143">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="1c609-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1c609-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="1c609-145">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="1c609-146">-Konum</span><span class="sxs-lookup"><span data-stu-id="1c609-146">-Location</span></span>
<span data-ttu-id="1c609-147">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-147">Specifies a location.</span></span>

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

### <span data-ttu-id="1c609-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="1c609-148">-OsType</span></span>
<span data-ttu-id="1c609-149">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="1c609-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1c609-150">-SkuName</span></span>
<span data-ttu-id="1c609-151">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="1c609-152">Kullanılabilir değerler Standard_LRS, Premium_LRS, StandardSSD_LRS ve UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="1c609-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="1c609-153">UltraSSD_LRS, Createoptıon parametresinde yalnızca boş değer ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1c609-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="1c609-154">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="1c609-154">-SourceResourceId</span></span>
<span data-ttu-id="1c609-155">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="1c609-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="1c609-156">-SourceUri</span></span>
<span data-ttu-id="1c609-157">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="1c609-158">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="1c609-158">-StorageAccountId</span></span>
<span data-ttu-id="1c609-159">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="1c609-160">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1c609-160">-Tag</span></span>
<span data-ttu-id="1c609-161">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1c609-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1c609-162">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1c609-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1c609-163">-Uploadsizeınbytes</span><span class="sxs-lookup"><span data-stu-id="1c609-163">-UploadSizeInBytes</span></span>
<span data-ttu-id="1c609-164">Createoptıon karşıya yüklendiğinde VHD altbilgisi dahil karşıya yükleme içeriğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-164">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="1c609-165">Bu değer, 20972032 (VHD alt bilgisinin 20 MIB + 512 baytı) ve 35183298347520 baytı (VHD altbilgisi için 32 TiB + 512 bytes) arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1c609-165">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="1c609-166">-Bölge</span><span class="sxs-lookup"><span data-stu-id="1c609-166">-Zone</span></span>
<span data-ttu-id="1c609-167">Diskin mantıksal bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c609-167">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="1c609-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c609-168">-Confirm</span></span>
<span data-ttu-id="1c609-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c609-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c609-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c609-170">-WhatIf</span></span>
<span data-ttu-id="1c609-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c609-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c609-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c609-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c609-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c609-173">CommonParameters</span></span>
<span data-ttu-id="1c609-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c609-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c609-175">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1c609-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c609-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c609-176">INPUTS</span></span>

### <span data-ttu-id="1c609-177">System. String</span><span class="sxs-lookup"><span data-stu-id="1c609-177">System.String</span></span>

### <span data-ttu-id="1c609-178">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1c609-178">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1c609-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1c609-179">System.Int32</span></span>

### <span data-ttu-id="1c609-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="1c609-180">System.String[]</span></span>

### <span data-ttu-id="1c609-181">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c609-181">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1c609-182">Microsoft. Azure. Management. COMPUTE. modeller. ımagediskreference</span><span class="sxs-lookup"><span data-stu-id="1c609-182">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="1c609-183">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="1c609-183">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1c609-184">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="1c609-184">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="1c609-185">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="1c609-185">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="1c609-186">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c609-186">OUTPUTS</span></span>

### <span data-ttu-id="1c609-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="1c609-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="1c609-188">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c609-188">NOTES</span></span>

## <span data-ttu-id="1c609-189">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c609-189">RELATED LINKS</span></span>
