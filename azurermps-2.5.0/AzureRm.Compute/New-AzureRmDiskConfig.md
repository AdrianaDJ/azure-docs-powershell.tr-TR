---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
ms.openlocfilehash: 8249bbb354d660f335316da503b0f19b6576fea6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939408"
---
# <span data-ttu-id="52ebf-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="52ebf-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="52ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="52ebf-103">Yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52ebf-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52ebf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52ebf-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ebf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52ebf-105">DESCRIPTION</span></span>
<span data-ttu-id="52ebf-106">**Yeni-AzureRmDiskConfig** cmdlet 'i, yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52ebf-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="52ebf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="52ebf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="52ebf-108">Example 1</span></span>
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

<span data-ttu-id="52ebf-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52ebf-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="52ebf-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="52ebf-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="52ebf-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="52ebf-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="52ebf-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52ebf-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="52ebf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52ebf-113">PARAMETERS</span></span>

### <span data-ttu-id="52ebf-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="52ebf-114">-CreateOption</span></span>
<span data-ttu-id="52ebf-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ebf-116">-DefaultProfile</span></span>
<span data-ttu-id="52ebf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52ebf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebf-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="52ebf-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="52ebf-119">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="52ebf-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="52ebf-120">-DiskSizeGB</span></span>
<span data-ttu-id="52ebf-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="52ebf-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="52ebf-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="52ebf-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="52ebf-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="52ebf-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="52ebf-124">-ImageReference</span></span>
<span data-ttu-id="52ebf-125">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="52ebf-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="52ebf-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="52ebf-127">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="52ebf-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="52ebf-128">-Location</span></span>
<span data-ttu-id="52ebf-129">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-129">Specifies a location.</span></span>

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

### <span data-ttu-id="52ebf-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="52ebf-130">-OsType</span></span>
<span data-ttu-id="52ebf-131">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="52ebf-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="52ebf-132">-SkuName</span></span>
<span data-ttu-id="52ebf-133">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebf-134">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="52ebf-134">-SourceResourceId</span></span>
<span data-ttu-id="52ebf-135">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="52ebf-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="52ebf-136">-SourceUri</span></span>
<span data-ttu-id="52ebf-137">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="52ebf-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="52ebf-138">-StorageAccountId</span></span>
<span data-ttu-id="52ebf-139">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="52ebf-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="52ebf-140">-Tag</span></span>
<span data-ttu-id="52ebf-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="52ebf-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="52ebf-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="52ebf-142">For example:</span></span>

<span data-ttu-id="52ebf-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="52ebf-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="52ebf-144">-Bölge</span><span class="sxs-lookup"><span data-stu-id="52ebf-144">-Zone</span></span>
<span data-ttu-id="52ebf-145">Diskin mantıksal bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-145">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebf-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="52ebf-146">-Confirm</span></span>
<span data-ttu-id="52ebf-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52ebf-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ebf-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ebf-148">-WhatIf</span></span>
<span data-ttu-id="52ebf-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52ebf-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52ebf-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52ebf-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ebf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ebf-151">CommonParameters</span></span>
<span data-ttu-id="52ebf-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52ebf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ebf-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ebf-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ebf-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52ebf-154">INPUTS</span></span>

### <span data-ttu-id="52ebf-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52ebf-155">None</span></span>
<span data-ttu-id="52ebf-156">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="52ebf-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52ebf-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52ebf-157">OUTPUTS</span></span>

### <span data-ttu-id="52ebf-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="52ebf-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="52ebf-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52ebf-159">NOTES</span></span>

## <span data-ttu-id="52ebf-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52ebf-160">RELATED LINKS</span></span>

