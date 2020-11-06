---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: b2c922a1dcce683636d61b68c66ab8cfb82535c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589875"
---
# <span data-ttu-id="0f754-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="0f754-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="0f754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f754-102">SYNOPSIS</span></span>
<span data-ttu-id="0f754-103">Yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f754-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f754-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f754-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f754-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f754-105">DESCRIPTION</span></span>
<span data-ttu-id="0f754-106">**Yeni-AzureRmDiskConfig** cmdlet 'i, yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f754-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="0f754-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f754-107">EXAMPLES</span></span>

### <span data-ttu-id="0f754-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0f754-108">Example 1</span></span>
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

<span data-ttu-id="0f754-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f754-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0f754-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="0f754-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0f754-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0f754-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="0f754-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f754-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0f754-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f754-113">PARAMETERS</span></span>

### <span data-ttu-id="0f754-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="0f754-114">-CreateOption</span></span>
<span data-ttu-id="0f754-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="0f754-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0f754-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="0f754-117">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-117">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0f754-118">-DiskSizeGB</span></span>
<span data-ttu-id="0f754-119">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-119">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0f754-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0f754-121">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="0f754-121">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="0f754-122">-ImageReference</span></span>
<span data-ttu-id="0f754-123">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-123">Specifies the image reference on a disk.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0f754-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="0f754-125">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-125">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="0f754-126">-Location</span></span>
<span data-ttu-id="0f754-127">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-127">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="0f754-128">-OsType</span></span>
<span data-ttu-id="0f754-129">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0f754-130">-SkuName</span></span>
<span data-ttu-id="0f754-131">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-132">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="0f754-132">-SourceResourceId</span></span>
<span data-ttu-id="0f754-133">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-133">Specifies the  source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="0f754-134">-SourceUri</span></span>
<span data-ttu-id="0f754-135">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-135">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-136">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="0f754-136">-StorageAccountId</span></span>
<span data-ttu-id="0f754-137">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-137">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0f754-138">-Tag</span></span>
<span data-ttu-id="0f754-139">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f754-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f754-140">-Confirm</span></span>
<span data-ttu-id="0f754-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f754-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f754-142">-WhatIf</span></span>
<span data-ttu-id="0f754-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f754-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f754-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f754-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f754-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f754-145">CommonParameters</span></span>
<span data-ttu-id="0f754-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f754-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f754-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f754-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f754-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f754-148">INPUTS</span></span>

### <span data-ttu-id="0f754-149">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0f754-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="0f754-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Koleksiyonlar. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0f754-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="0f754-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f754-151">OUTPUTS</span></span>

### <span data-ttu-id="0f754-152">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="0f754-152">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="0f754-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f754-153">NOTES</span></span>

## <span data-ttu-id="0f754-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f754-154">RELATED LINKS</span></span>

