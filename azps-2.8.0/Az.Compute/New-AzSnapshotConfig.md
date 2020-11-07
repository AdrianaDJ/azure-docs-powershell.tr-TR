---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: c42aae31bb525f9da6a2963a945a6244373ac8db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752840"
---
# <span data-ttu-id="cfe82-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cfe82-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="cfe82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe82-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe82-103">Yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfe82-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="cfe82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfe82-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfe82-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe82-106">**Yeni-AzSnapshotConfig** cmdlet 'i yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfe82-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="cfe82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfe82-107">EXAMPLES</span></span>

### <span data-ttu-id="cfe82-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cfe82-108">Example 1</span></span>
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

<span data-ttu-id="cfe82-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfe82-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="cfe82-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="cfe82-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="cfe82-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cfe82-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="cfe82-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfe82-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cfe82-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfe82-113">PARAMETERS</span></span>

### <span data-ttu-id="cfe82-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="cfe82-114">-CreateOption</span></span>
<span data-ttu-id="cfe82-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="cfe82-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe82-116">-DefaultProfile</span></span>
<span data-ttu-id="cfe82-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cfe82-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfe82-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cfe82-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="cfe82-119">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="cfe82-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="cfe82-120">-DiskSizeGB</span></span>
<span data-ttu-id="cfe82-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="cfe82-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="cfe82-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="cfe82-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="cfe82-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="cfe82-124">-Hiper VCR</span><span class="sxs-lookup"><span data-stu-id="cfe82-124">-HyperVGeneration</span></span>
<span data-ttu-id="cfe82-125">Sanal makinenin Hiper Yöneticisi üretimi.</span><span class="sxs-lookup"><span data-stu-id="cfe82-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="cfe82-126">Yalnızca işletim sistemi disklerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="cfe82-127">İzin verilen değerler v1 ve v2.</span><span class="sxs-lookup"><span data-stu-id="cfe82-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="cfe82-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="cfe82-128">-ImageReference</span></span>
<span data-ttu-id="cfe82-129">Anlık görüntüdeki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="cfe82-130">-Artımlı</span><span class="sxs-lookup"><span data-stu-id="cfe82-130">-Incremental</span></span>
<span data-ttu-id="cfe82-131">Artımlı bir anlık görüntü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-131">Specifies an incremental snapshot.</span></span> <span data-ttu-id="cfe82-132">Aynı diskteki Artımlı anlık görüntüler tam anlık görüntülerle daha az yer kaplar ve dağıtılmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-132">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="cfe82-133">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cfe82-133">-KeyEncryptionKey</span></span>
<span data-ttu-id="cfe82-134">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-134">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="cfe82-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="cfe82-135">-Location</span></span>
<span data-ttu-id="cfe82-136">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-136">Specifies a location.</span></span>

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

### <span data-ttu-id="cfe82-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="cfe82-137">-OsType</span></span>
<span data-ttu-id="cfe82-138">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-138">Specifies the OS type.</span></span>

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

### <span data-ttu-id="cfe82-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cfe82-139">-SkuName</span></span>
<span data-ttu-id="cfe82-140">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-140">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="cfe82-141">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="cfe82-141">-SourceResourceId</span></span>
<span data-ttu-id="cfe82-142">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-142">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="cfe82-143">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="cfe82-143">-SourceUri</span></span>
<span data-ttu-id="cfe82-144">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-144">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="cfe82-145">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="cfe82-145">-StorageAccountId</span></span>
<span data-ttu-id="cfe82-146">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-146">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="cfe82-147">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cfe82-147">-Tag</span></span>
<span data-ttu-id="cfe82-148">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="cfe82-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cfe82-149">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="cfe82-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cfe82-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="cfe82-150">-Confirm</span></span>
<span data-ttu-id="cfe82-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cfe82-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe82-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe82-152">-WhatIf</span></span>
<span data-ttu-id="cfe82-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cfe82-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfe82-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cfe82-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe82-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe82-155">CommonParameters</span></span>
<span data-ttu-id="cfe82-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfe82-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe82-157">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cfe82-157">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe82-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfe82-158">INPUTS</span></span>

### <span data-ttu-id="cfe82-159">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe82-159">System.String</span></span>

### <span data-ttu-id="cfe82-160">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cfe82-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cfe82-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cfe82-161">System.Int32</span></span>

### <span data-ttu-id="cfe82-162">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfe82-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cfe82-163">Microsoft. Azure. Management. COMPUTE. modeller. ımagediskreference</span><span class="sxs-lookup"><span data-stu-id="cfe82-163">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="cfe82-164">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="cfe82-164">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cfe82-165">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="cfe82-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="cfe82-166">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="cfe82-166">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="cfe82-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfe82-167">OUTPUTS</span></span>

### <span data-ttu-id="cfe82-168">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="cfe82-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="cfe82-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfe82-169">NOTES</span></span>

## <span data-ttu-id="cfe82-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfe82-170">RELATED LINKS</span></span>
