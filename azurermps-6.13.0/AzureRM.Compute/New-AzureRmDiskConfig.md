---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763003"
---
# <span data-ttu-id="beee8-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="beee8-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="beee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beee8-102">SYNOPSIS</span></span>
<span data-ttu-id="beee8-103">Yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="beee8-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beee8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="beee8-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="beee8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="beee8-105">DESCRIPTION</span></span>
<span data-ttu-id="beee8-106">**Yeni-AzureRmDiskConfig** cmdlet 'i, yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="beee8-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="beee8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="beee8-107">EXAMPLES</span></span>

### <span data-ttu-id="beee8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="beee8-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="beee8-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="beee8-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="beee8-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="beee8-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="beee8-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="beee8-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="beee8-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="beee8-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="beee8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="beee8-113">PARAMETERS</span></span>

### <span data-ttu-id="beee8-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="beee8-114">-CreateOption</span></span>
<span data-ttu-id="beee8-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="beee8-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="beee8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beee8-116">-DefaultProfile</span></span>
<span data-ttu-id="beee8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="beee8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beee8-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="beee8-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="beee8-119">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="beee8-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="beee8-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="beee8-121">Bu diskte izin verilen ıOPS sayısı; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="beee8-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="beee8-122">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="beee8-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="beee8-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="beee8-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="beee8-124">Bu diskte izin verilen bant genişliği; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="beee8-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="beee8-125">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="beee8-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="beee8-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="beee8-126">-DiskSizeGB</span></span>
<span data-ttu-id="beee8-127">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="beee8-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="beee8-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="beee8-129">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="beee8-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="beee8-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="beee8-130">-ImageReference</span></span>
<span data-ttu-id="beee8-131">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="beee8-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="beee8-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="beee8-133">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="beee8-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="beee8-134">-Location</span></span>
<span data-ttu-id="beee8-135">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-135">Specifies a location.</span></span>

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

### <span data-ttu-id="beee8-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="beee8-136">-OsType</span></span>
<span data-ttu-id="beee8-137">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="beee8-138">-SkuName</span><span class="sxs-lookup"><span data-stu-id="beee8-138">-SkuName</span></span>
<span data-ttu-id="beee8-139">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="beee8-140">Kullanılabilir değerler Standard_LRS, Premium_LRS, StandardSSD_LRS ve UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="beee8-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="beee8-141">UltraSSD_LRS, Createoptıon parametresinde yalnızca boş değer ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="beee8-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="beee8-142">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="beee8-142">-SourceResourceId</span></span>
<span data-ttu-id="beee8-143">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="beee8-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="beee8-144">-SourceUri</span></span>
<span data-ttu-id="beee8-145">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="beee8-146">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="beee8-146">-StorageAccountId</span></span>
<span data-ttu-id="beee8-147">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="beee8-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="beee8-148">-Tag</span></span>
<span data-ttu-id="beee8-149">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="beee8-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="beee8-150">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="beee8-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="beee8-151">-Bölge</span><span class="sxs-lookup"><span data-stu-id="beee8-151">-Zone</span></span>
<span data-ttu-id="beee8-152">Diskin mantıksal bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee8-152">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="beee8-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="beee8-153">-Confirm</span></span>
<span data-ttu-id="beee8-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="beee8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beee8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beee8-155">-WhatIf</span></span>
<span data-ttu-id="beee8-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="beee8-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="beee8-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="beee8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beee8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beee8-158">CommonParameters</span></span>
<span data-ttu-id="beee8-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="beee8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beee8-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beee8-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beee8-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="beee8-161">INPUTS</span></span>

### <span data-ttu-id="beee8-162">System. String</span><span class="sxs-lookup"><span data-stu-id="beee8-162">System.String</span></span>

### <span data-ttu-id="beee8-163">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="beee8-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="beee8-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="beee8-164">System.Int32</span></span>

### <span data-ttu-id="beee8-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="beee8-165">System.String[]</span></span>

### <span data-ttu-id="beee8-166">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="beee8-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="beee8-167">Microsoft. Azure. Management. COMPUTE. modeller. ımagediskreference</span><span class="sxs-lookup"><span data-stu-id="beee8-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="beee8-168">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="beee8-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="beee8-169">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="beee8-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="beee8-170">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="beee8-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="beee8-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="beee8-171">OUTPUTS</span></span>

### <span data-ttu-id="beee8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="beee8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="beee8-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="beee8-173">NOTES</span></span>

## <span data-ttu-id="beee8-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="beee8-174">RELATED LINKS</span></span>
