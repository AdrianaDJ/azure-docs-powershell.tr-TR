---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
ms.openlocfilehash: 1aee03af5a326585f9578a2f3eef378c3b783431
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594448"
---
# <span data-ttu-id="e2b02-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e2b02-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="e2b02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2b02-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b02-103">Yapılandırılabilir bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2b02-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2b02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2b02-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2b02-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2b02-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b02-106">**Yeni-AzureRmDiskUpdateConfig** cmdlet 'i, yapılandırılabilir bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2b02-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="e2b02-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2b02-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b02-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2b02-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="e2b02-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2b02-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="e2b02-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="e2b02-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="e2b02-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e2b02-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="e2b02-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e2b02-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e2b02-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="e2b02-114">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı mevcut diski 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="e2b02-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2b02-115">PARAMETERS</span></span>

### <span data-ttu-id="e2b02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b02-116">-DefaultProfile</span></span>
<span data-ttu-id="e2b02-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2b02-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2b02-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e2b02-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="e2b02-119">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="e2b02-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="e2b02-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="e2b02-121">Bu diskte izin verilen ıOPS sayısı; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e2b02-122">Bir işlem 4k ile 256k bayt arasında aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="e2b02-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="e2b02-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="e2b02-124">Bu diskte izin verilen bant genişliği; yalnızca UltraSSD diskleri için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e2b02-125">MB/sn, 10 ' un en yüksek bit sayısı olan ISO gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e2b02-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="e2b02-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e2b02-126">-DiskSizeGB</span></span>
<span data-ttu-id="e2b02-127">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e2b02-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e2b02-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e2b02-129">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="e2b02-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e2b02-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e2b02-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="e2b02-131">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-131">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="e2b02-132">-OsType</span><span class="sxs-lookup"><span data-stu-id="e2b02-132">-OsType</span></span>
<span data-ttu-id="e2b02-133">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-133">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e2b02-134">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e2b02-134">-SkuName</span></span>
<span data-ttu-id="e2b02-135">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-135">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="e2b02-136">Kullanılabilir değerler Standard_LRS, Premium_LRS, StandardSSD_LRS ve UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="e2b02-136">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="e2b02-137">UltraSSD_LRS, Createoptıon parametresinde yalnızca boş değer ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-137">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="e2b02-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e2b02-138">-Tag</span></span>
<span data-ttu-id="e2b02-139">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e2b02-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e2b02-140">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e2b02-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e2b02-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2b02-141">-Confirm</span></span>
<span data-ttu-id="e2b02-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2b02-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b02-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b02-143">-WhatIf</span></span>
<span data-ttu-id="e2b02-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2b02-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2b02-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2b02-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b02-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b02-146">CommonParameters</span></span>
<span data-ttu-id="e2b02-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2b02-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b02-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b02-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b02-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2b02-149">INPUTS</span></span>

### <span data-ttu-id="e2b02-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e2b02-150">System.String</span></span>

### <span data-ttu-id="e2b02-151">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e2b02-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e2b02-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e2b02-152">System.Int32</span></span>

### <span data-ttu-id="e2b02-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e2b02-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e2b02-154">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e2b02-154">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e2b02-155">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="e2b02-155">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="e2b02-156">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="e2b02-156">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="e2b02-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2b02-157">OUTPUTS</span></span>

### <span data-ttu-id="e2b02-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsReference</span><span class="sxs-lookup"><span data-stu-id="e2b02-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="e2b02-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2b02-159">NOTES</span></span>

## <span data-ttu-id="e2b02-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2b02-160">RELATED LINKS</span></span>
