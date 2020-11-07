---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 2989a5be6ef6eee137f296ab1379931070082fe9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937642"
---
# <span data-ttu-id="55d31-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="55d31-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="55d31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55d31-102">SYNOPSIS</span></span>
<span data-ttu-id="55d31-103">Yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55d31-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="55d31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55d31-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55d31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55d31-105">DESCRIPTION</span></span>
<span data-ttu-id="55d31-106">**Yeni-AzSnapshotConfig** cmdlet 'i yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55d31-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="55d31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55d31-107">EXAMPLES</span></span>

### <span data-ttu-id="55d31-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55d31-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="55d31-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55d31-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="55d31-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="55d31-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="55d31-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55d31-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="55d31-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55d31-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="55d31-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55d31-113">PARAMETERS</span></span>

### <span data-ttu-id="55d31-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="55d31-114">-CreateOption</span></span>
<span data-ttu-id="55d31-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="55d31-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="55d31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d31-116">-DefaultProfile</span></span>
<span data-ttu-id="55d31-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55d31-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55d31-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="55d31-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="55d31-119">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="55d31-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="55d31-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="55d31-121">Rest 'de şifrelemeyi etkinleştirmek için kullanılacak disk şifrelemesi kümesi kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="55d31-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="55d31-122">-DiskSizeGB</span></span>
<span data-ttu-id="55d31-123">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="55d31-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="55d31-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="55d31-125">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="55d31-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="55d31-126">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="55d31-126">-EncryptionType</span></span>
<span data-ttu-id="55d31-127">Diskin verilerini şifrelemek için kullanılan anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="55d31-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="55d31-128">Kullanılabilir değerler şunlardır: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="55d31-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="55d31-129">-Hiper VCR</span><span class="sxs-lookup"><span data-stu-id="55d31-129">-HyperVGeneration</span></span>
<span data-ttu-id="55d31-130">Sanal makinenin Hiper Yöneticisi üretimi.</span><span class="sxs-lookup"><span data-stu-id="55d31-130">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="55d31-131">Yalnızca işletim sistemi disklerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="55d31-131">Applicable to OS disks only.</span></span>  <span data-ttu-id="55d31-132">İzin verilen değerler v1 ve v2.</span><span class="sxs-lookup"><span data-stu-id="55d31-132">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="55d31-133">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="55d31-133">-ImageReference</span></span>
<span data-ttu-id="55d31-134">Anlık görüntüdeki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-134">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="55d31-135">-Artımlı</span><span class="sxs-lookup"><span data-stu-id="55d31-135">-Incremental</span></span>
<span data-ttu-id="55d31-136">Artımlı bir anlık görüntü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-136">Specifies an incremental snapshot.</span></span> <span data-ttu-id="55d31-137">Aynı diskteki Artımlı anlık görüntüler tam anlık görüntülerle daha az yer kaplar ve dağıtılmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="55d31-137">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d31-138">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="55d31-138">-KeyEncryptionKey</span></span>
<span data-ttu-id="55d31-139">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-139">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="55d31-140">-Konum</span><span class="sxs-lookup"><span data-stu-id="55d31-140">-Location</span></span>
<span data-ttu-id="55d31-141">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-141">Specifies a location.</span></span>

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

### <span data-ttu-id="55d31-142">-OsType</span><span class="sxs-lookup"><span data-stu-id="55d31-142">-OsType</span></span>
<span data-ttu-id="55d31-143">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-143">Specifies the OS type.</span></span>

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

### <span data-ttu-id="55d31-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="55d31-144">-SkuName</span></span>
<span data-ttu-id="55d31-145">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-145">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="55d31-146">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="55d31-146">-SourceResourceId</span></span>
<span data-ttu-id="55d31-147">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-147">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="55d31-148">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="55d31-148">-SourceUri</span></span>
<span data-ttu-id="55d31-149">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-149">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="55d31-150">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="55d31-150">-StorageAccountId</span></span>
<span data-ttu-id="55d31-151">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="55d31-151">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="55d31-152">Etiketli</span><span class="sxs-lookup"><span data-stu-id="55d31-152">-Tag</span></span>
<span data-ttu-id="55d31-153">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="55d31-153">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55d31-154">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="55d31-154">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55d31-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="55d31-155">-Confirm</span></span>
<span data-ttu-id="55d31-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55d31-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55d31-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55d31-157">-WhatIf</span></span>
<span data-ttu-id="55d31-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55d31-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55d31-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55d31-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55d31-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d31-160">CommonParameters</span></span>
<span data-ttu-id="55d31-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55d31-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d31-162">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55d31-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d31-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55d31-163">INPUTS</span></span>

### <span data-ttu-id="55d31-164">System. String</span><span class="sxs-lookup"><span data-stu-id="55d31-164">System.String</span></span>

### <span data-ttu-id="55d31-165">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="55d31-165">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="55d31-166">System. Int32</span><span class="sxs-lookup"><span data-stu-id="55d31-166">System.Int32</span></span>

### <span data-ttu-id="55d31-167">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55d31-167">System.Collections.Hashtable</span></span>

### <span data-ttu-id="55d31-168">Microsoft. Azure. Management. COMPUTE. modeller. ımagediskreference</span><span class="sxs-lookup"><span data-stu-id="55d31-168">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="55d31-169">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="55d31-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="55d31-170">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="55d31-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="55d31-171">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="55d31-171">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="55d31-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55d31-172">OUTPUTS</span></span>

### <span data-ttu-id="55d31-173">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="55d31-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="55d31-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55d31-174">NOTES</span></span>

## <span data-ttu-id="55d31-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55d31-175">RELATED LINKS</span></span>
