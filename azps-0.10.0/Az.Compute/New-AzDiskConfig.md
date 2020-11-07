---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 851687bdc00b25bd283433fbc00254380a8ef3a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936975"
---
# <span data-ttu-id="4a1d9-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4a1d9-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="4a1d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1d9-103">Yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="4a1d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a1d9-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a1d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a1d9-105">DESCRIPTION</span></span>
<span data-ttu-id="4a1d9-106">**New-AzDiskConfig** cmdlet 'i yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="4a1d9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a1d9-107">EXAMPLES</span></span>

### <span data-ttu-id="4a1d9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4a1d9-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="4a1d9-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="4a1d9-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="4a1d9-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="4a1d9-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4a1d9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a1d9-113">PARAMETERS</span></span>

### <span data-ttu-id="4a1d9-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="4a1d9-114">-CreateOption</span></span>
<span data-ttu-id="4a1d9-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="4a1d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1d9-116">-DefaultProfile</span></span>
<span data-ttu-id="4a1d9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a1d9-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4a1d9-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="4a1d9-119">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="4a1d9-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="4a1d9-120">-DiskSizeGB</span></span>
<span data-ttu-id="4a1d9-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="4a1d9-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="4a1d9-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="4a1d9-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="4a1d9-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="4a1d9-124">-ImageReference</span></span>
<span data-ttu-id="4a1d9-125">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="4a1d9-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4a1d9-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="4a1d9-127">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="4a1d9-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="4a1d9-128">-Location</span></span>
<span data-ttu-id="4a1d9-129">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-129">Specifies a location.</span></span>

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

### <span data-ttu-id="4a1d9-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="4a1d9-130">-OsType</span></span>
<span data-ttu-id="4a1d9-131">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="4a1d9-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4a1d9-132">-SkuName</span></span>
<span data-ttu-id="4a1d9-133">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="4a1d9-134">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="4a1d9-134">-SourceResourceId</span></span>
<span data-ttu-id="4a1d9-135">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="4a1d9-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="4a1d9-136">-SourceUri</span></span>
<span data-ttu-id="4a1d9-137">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="4a1d9-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="4a1d9-138">-StorageAccountId</span></span>
<span data-ttu-id="4a1d9-139">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="4a1d9-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4a1d9-140">-Tag</span></span>
<span data-ttu-id="4a1d9-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4a1d9-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4a1d9-142">For example:</span></span>

<span data-ttu-id="4a1d9-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4a1d9-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4a1d9-144">-Bölge</span><span class="sxs-lookup"><span data-stu-id="4a1d9-144">-Zone</span></span>
<span data-ttu-id="4a1d9-145">Diskin mantıksal bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-145">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="4a1d9-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a1d9-146">-Confirm</span></span>
<span data-ttu-id="4a1d9-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a1d9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a1d9-148">-WhatIf</span></span>
<span data-ttu-id="4a1d9-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a1d9-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a1d9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1d9-151">CommonParameters</span></span>
<span data-ttu-id="4a1d9-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1d9-153">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a1d9-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1d9-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a1d9-154">INPUTS</span></span>

### <span data-ttu-id="4a1d9-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4a1d9-155">None</span></span>
<span data-ttu-id="4a1d9-156">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4a1d9-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a1d9-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a1d9-157">OUTPUTS</span></span>

### <span data-ttu-id="4a1d9-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="4a1d9-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="4a1d9-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a1d9-159">NOTES</span></span>

## <span data-ttu-id="4a1d9-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a1d9-160">RELATED LINKS</span></span>

