---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276244"
---
# <span data-ttu-id="5ffb5-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="5ffb5-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="5ffb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ffb5-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffb5-103">Yapılandırılabilir bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="5ffb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ffb5-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ffb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ffb5-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffb5-106">**New-AzDiskUpdateConfig** cmdlet 'i yapılandırılabilir bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="5ffb5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ffb5-107">EXAMPLES</span></span>

### <span data-ttu-id="5ffb5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ffb5-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="5ffb5-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="5ffb5-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="5ffb5-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="5ffb5-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="5ffb5-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5ffb5-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="5ffb5-114">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı mevcut diski 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="5ffb5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ffb5-115">PARAMETERS</span></span>

### <span data-ttu-id="5ffb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffb5-116">-DefaultProfile</span></span>
<span data-ttu-id="5ffb5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ffb5-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="5ffb5-118">-DiskAccessId</span></span>
<span data-ttu-id="5ffb5-119">{{Fill Dıskaccessid açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="5ffb5-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="5ffb5-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5ffb5-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="5ffb5-121">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="5ffb5-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="5ffb5-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="5ffb5-123">Rest 'de şifrelemeyi etkinleştirmek için kullanılacak disk şifrelemesi kümesi kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="5ffb5-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="5ffb5-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="5ffb5-125">Tüm VM 'lerde izin verilecek toplam ıOPS sayısı, paylaşılan diski salt okunur olarak bağlama.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="5ffb5-126">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-126">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="5ffb5-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="5ffb5-128">Bu diskte izin verilen ıOPS sayısı; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="5ffb5-129">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-129">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="5ffb5-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="5ffb5-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="5ffb5-131">Tüm VM 'lerde izin verilen toplam işleme (MBps) paylaşılan diski ReadOnly olarak bağlama.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="5ffb5-132">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="5ffb5-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="5ffb5-134">Bu diskte izin verilen bant genişliği; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="5ffb5-135">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="5ffb5-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="5ffb5-136">-DiskSizeGB</span></span>
<span data-ttu-id="5ffb5-137">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-137">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="5ffb5-138">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="5ffb5-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="5ffb5-139">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-139">Enable encryption settings.</span></span>

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

### <span data-ttu-id="5ffb5-140">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="5ffb5-140">-EncryptionType</span></span>
<span data-ttu-id="5ffb5-141">Diskin verilerini şifrelemek için kullanılan anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="5ffb5-142">Kullanılabilir değerler şunlardır: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="5ffb5-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="5ffb5-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5ffb5-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="5ffb5-144">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-144">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="5ffb5-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="5ffb5-145">-MaxSharesCount</span></span>
<span data-ttu-id="5ffb5-146">Diske aynı anda iliştirileceği en fazla VM sayısı.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="5ffb5-147">Birden büyük değer aynı anda birden fazla VM 'ye takılacak bir diski belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="5ffb5-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5ffb5-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="5ffb5-149">{{Fill NetworkAccessPolicy açıklama}}</span><span class="sxs-lookup"><span data-stu-id="5ffb5-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="5ffb5-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="5ffb5-150">-OsType</span></span>
<span data-ttu-id="5ffb5-151">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="5ffb5-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5ffb5-152">-SkuName</span></span>
<span data-ttu-id="5ffb5-153">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="5ffb5-154">Kullanılabilir değerler Standard_LRS, Premium_LRS, StandardSSD_LRS ve UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="5ffb5-155">UltraSSD_LRS, Createoptıon parametresinde yalnızca boş değer ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="5ffb5-156">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5ffb5-156">-Tag</span></span>
<span data-ttu-id="5ffb5-157">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5ffb5-158">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="5ffb5-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffb5-159">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="5ffb5-159">-Tier</span></span>
<span data-ttu-id="5ffb5-160">Diskin performans katmanı.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-160">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="5ffb5-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ffb5-161">-Confirm</span></span>
<span data-ttu-id="5ffb5-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ffb5-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ffb5-163">-WhatIf</span></span>
<span data-ttu-id="5ffb5-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ffb5-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ffb5-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffb5-166">CommonParameters</span></span>
<span data-ttu-id="5ffb5-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffb5-168">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5ffb5-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffb5-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ffb5-169">INPUTS</span></span>

### <span data-ttu-id="5ffb5-170">System. String</span><span class="sxs-lookup"><span data-stu-id="5ffb5-170">System.String</span></span>

### <span data-ttu-id="5ffb5-171">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5ffb5-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5ffb5-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5ffb5-172">System.Int32</span></span>

### <span data-ttu-id="5ffb5-173">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5ffb5-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5ffb5-174">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ffb5-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5ffb5-175">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="5ffb5-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="5ffb5-176">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="5ffb5-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="5ffb5-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ffb5-177">OUTPUTS</span></span>

### <span data-ttu-id="5ffb5-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsReference</span><span class="sxs-lookup"><span data-stu-id="5ffb5-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="5ffb5-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ffb5-179">NOTES</span></span>

## <span data-ttu-id="5ffb5-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ffb5-180">RELATED LINKS</span></span>
