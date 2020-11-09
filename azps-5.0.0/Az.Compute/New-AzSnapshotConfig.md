---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 5d9a48fbdc323ffdd232d6d961da6564fecc0dff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323353"
---
# <span data-ttu-id="a6938-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a6938-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="a6938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6938-102">SYNOPSIS</span></span>
<span data-ttu-id="a6938-103">Yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6938-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="a6938-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6938-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6938-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6938-105">DESCRIPTION</span></span>
<span data-ttu-id="a6938-106">**Yeni-AzSnapshotConfig** cmdlet 'i yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6938-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="a6938-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6938-107">EXAMPLES</span></span>

### <span data-ttu-id="a6938-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a6938-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="a6938-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6938-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="a6938-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="a6938-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a6938-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a6938-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="a6938-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6938-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a6938-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a6938-113">Example 2</span></span>

<span data-ttu-id="a6938-114">Yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6938-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="a6938-115">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="a6938-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="a6938-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6938-116">PARAMETERS</span></span>

### <span data-ttu-id="a6938-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="a6938-117">-CreateOption</span></span>
<span data-ttu-id="a6938-118">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="a6938-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="a6938-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6938-119">-DefaultProfile</span></span>
<span data-ttu-id="a6938-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6938-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6938-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a6938-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="a6938-122">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="a6938-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a6938-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a6938-124">Rest 'de şifrelemeyi etkinleştirmek için kullanılacak disk şifrelemesi kümesi kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="a6938-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a6938-125">-DiskSizeGB</span></span>
<span data-ttu-id="a6938-126">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a6938-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a6938-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a6938-128">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a6938-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a6938-129">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="a6938-129">-EncryptionType</span></span>
<span data-ttu-id="a6938-130">Diskin verilerini şifrelemek için kullanılan anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="a6938-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="a6938-131">Kullanılabilir değerler şunlardır: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="a6938-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="a6938-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="a6938-132">-DiskAccessId</span></span>
<span data-ttu-id="a6938-133">Özel uç noktaları kullanmak için DiskAccess kaynağının ARM kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a6938-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="a6938-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a6938-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="a6938-135">Ağ erişimi ilkesi, ağ erişim ilkesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a6938-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="a6938-136">Olası değerler: ' AllowAll ', ' AllowPrivate ', ' DenyAll '</span><span class="sxs-lookup"><span data-stu-id="a6938-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="a6938-137">-Hiper VCR</span><span class="sxs-lookup"><span data-stu-id="a6938-137">-HyperVGeneration</span></span>
<span data-ttu-id="a6938-138">Sanal makinenin Hiper Yöneticisi üretimi.</span><span class="sxs-lookup"><span data-stu-id="a6938-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="a6938-139">Yalnızca işletim sistemi disklerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="a6938-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="a6938-140">İzin verilen değerler v1 ve v2.</span><span class="sxs-lookup"><span data-stu-id="a6938-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="a6938-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="a6938-141">-ImageReference</span></span>
<span data-ttu-id="a6938-142">Anlık görüntüdeki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-142">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="a6938-143">-Artımlı</span><span class="sxs-lookup"><span data-stu-id="a6938-143">-Incremental</span></span>
<span data-ttu-id="a6938-144">Artımlı bir anlık görüntü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="a6938-145">Aynı diskteki Artımlı anlık görüntüler tam anlık görüntülerle daha az yer kaplar ve dağıtılmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="a6938-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="a6938-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a6938-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="a6938-147">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="a6938-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="a6938-148">-Location</span></span>
<span data-ttu-id="a6938-149">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-149">Specifies a location.</span></span>

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

### <span data-ttu-id="a6938-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="a6938-150">-OsType</span></span>
<span data-ttu-id="a6938-151">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a6938-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a6938-152">-SkuName</span></span>
<span data-ttu-id="a6938-153">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="a6938-154">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="a6938-154">-SourceResourceId</span></span>
<span data-ttu-id="a6938-155">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="a6938-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="a6938-156">-SourceUri</span></span>
<span data-ttu-id="a6938-157">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="a6938-158">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="a6938-158">-StorageAccountId</span></span>
<span data-ttu-id="a6938-159">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6938-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="a6938-160">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a6938-160">-Tag</span></span>
<span data-ttu-id="a6938-161">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="a6938-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a6938-162">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="a6938-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a6938-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6938-163">-Confirm</span></span>
<span data-ttu-id="a6938-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6938-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6938-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6938-165">-WhatIf</span></span>
<span data-ttu-id="a6938-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6938-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6938-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6938-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6938-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6938-168">CommonParameters</span></span>
<span data-ttu-id="a6938-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6938-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6938-170">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a6938-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6938-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6938-171">INPUTS</span></span>

### <span data-ttu-id="a6938-172">System. String</span><span class="sxs-lookup"><span data-stu-id="a6938-172">System.String</span></span>

### <span data-ttu-id="a6938-173">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a6938-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a6938-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a6938-174">System.Int32</span></span>

### <span data-ttu-id="a6938-175">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a6938-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a6938-176">Microsoft. Azure. Management. COMPUTE. modeller. ımagediskreference</span><span class="sxs-lookup"><span data-stu-id="a6938-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="a6938-177">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a6938-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a6938-178">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="a6938-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="a6938-179">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="a6938-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="a6938-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6938-180">OUTPUTS</span></span>

### <span data-ttu-id="a6938-181">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6938-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="a6938-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6938-182">NOTES</span></span>

## <span data-ttu-id="a6938-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6938-183">RELATED LINKS</span></span>
