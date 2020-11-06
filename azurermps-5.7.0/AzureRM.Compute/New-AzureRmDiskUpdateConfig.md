---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
ms.openlocfilehash: 68a6e53e6ad024411c0775a21bbdbb0d0b8c75f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589874"
---
# <span data-ttu-id="aefc7-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="aefc7-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="aefc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aefc7-102">SYNOPSIS</span></span>
<span data-ttu-id="aefc7-103">Yapılandırılabilir bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefc7-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aefc7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aefc7-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aefc7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aefc7-105">DESCRIPTION</span></span>
<span data-ttu-id="aefc7-106">**Yeni-AzureRmDiskUpdateConfig** cmdlet 'i, yapılandırılabilir bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefc7-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="aefc7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aefc7-107">EXAMPLES</span></span>

### <span data-ttu-id="aefc7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aefc7-108">Example 1</span></span>
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

<span data-ttu-id="aefc7-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefc7-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="aefc7-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="aefc7-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="aefc7-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aefc7-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="aefc7-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="aefc7-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="aefc7-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="aefc7-114">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı mevcut diski 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="aefc7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aefc7-115">PARAMETERS</span></span>

### <span data-ttu-id="aefc7-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="aefc7-116">-CreateOption</span></span>
<span data-ttu-id="aefc7-117">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-117">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="aefc7-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aefc7-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="aefc7-119">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="aefc7-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="aefc7-120">-DiskSizeGB</span></span>
<span data-ttu-id="aefc7-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="aefc7-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="aefc7-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="aefc7-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="aefc7-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="aefc7-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="aefc7-124">-ImageReference</span></span>
<span data-ttu-id="aefc7-125">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="aefc7-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aefc7-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="aefc7-127">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="aefc7-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="aefc7-128">-OsType</span></span>
<span data-ttu-id="aefc7-129">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="aefc7-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="aefc7-130">-SkuName</span></span>
<span data-ttu-id="aefc7-131">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="aefc7-132">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="aefc7-132">-SourceResourceId</span></span>
<span data-ttu-id="aefc7-133">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="aefc7-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="aefc7-134">-SourceUri</span></span>
<span data-ttu-id="aefc7-135">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="aefc7-136">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="aefc7-136">-StorageAccountId</span></span>
<span data-ttu-id="aefc7-137">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="aefc7-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="aefc7-138">-Tag</span></span>
<span data-ttu-id="aefc7-139">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aefc7-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="aefc7-140">-Confirm</span></span>
<span data-ttu-id="aefc7-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aefc7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aefc7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefc7-142">-WhatIf</span></span>
<span data-ttu-id="aefc7-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aefc7-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aefc7-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aefc7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aefc7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefc7-145">CommonParameters</span></span>
<span data-ttu-id="aefc7-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aefc7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefc7-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aefc7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefc7-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aefc7-148">INPUTS</span></span>

### <span data-ttu-id="aefc7-149">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="aefc7-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="aefc7-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Koleksiyonlar. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aefc7-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="aefc7-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aefc7-151">OUTPUTS</span></span>

### <span data-ttu-id="aefc7-152">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="aefc7-152">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="aefc7-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aefc7-153">NOTES</span></span>

## <span data-ttu-id="aefc7-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aefc7-154">RELATED LINKS</span></span>

