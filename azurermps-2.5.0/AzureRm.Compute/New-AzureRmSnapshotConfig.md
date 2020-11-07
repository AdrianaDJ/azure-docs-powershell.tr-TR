---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
ms.openlocfilehash: a18eb8513e419d174efac9179cb65fe175d12dd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939951"
---
# <span data-ttu-id="e1c1c-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e1c1c-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="e1c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c1c-103">Yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1c1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1c1c-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c1c-106">**Yeni-AzureRmSnapshotConfig** cmdlet 'i, yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="e1c1c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c1c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e1c1c-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="e1c1c-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="e1c1c-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e1c1c-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="e1c1c-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e1c1c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1c1c-113">PARAMETERS</span></span>

### <span data-ttu-id="e1c1c-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e1c1c-114">-CreateOption</span></span>
<span data-ttu-id="e1c1c-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="e1c1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c1c-116">-DefaultProfile</span></span>
<span data-ttu-id="e1c1c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1c1c-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e1c1c-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="e1c1c-119">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="e1c1c-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e1c1c-120">-DiskSizeGB</span></span>
<span data-ttu-id="e1c1c-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e1c1c-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e1c1c-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e1c1c-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e1c1c-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="e1c1c-124">-ImageReference</span></span>
<span data-ttu-id="e1c1c-125">Anlık görüntüdeki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="e1c1c-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e1c1c-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="e1c1c-127">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="e1c1c-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="e1c1c-128">-Location</span></span>
<span data-ttu-id="e1c1c-129">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-129">Specifies a location.</span></span>

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

### <span data-ttu-id="e1c1c-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="e1c1c-130">-OsType</span></span>
<span data-ttu-id="e1c1c-131">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e1c1c-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e1c1c-132">-SkuName</span></span>
<span data-ttu-id="e1c1c-133">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="e1c1c-134">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="e1c1c-134">-SourceResourceId</span></span>
<span data-ttu-id="e1c1c-135">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="e1c1c-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="e1c1c-136">-SourceUri</span></span>
<span data-ttu-id="e1c1c-137">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="e1c1c-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="e1c1c-138">-StorageAccountId</span></span>
<span data-ttu-id="e1c1c-139">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="e1c1c-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e1c1c-140">-Tag</span></span>
<span data-ttu-id="e1c1c-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e1c1c-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="e1c1c-142">For example:</span></span>

<span data-ttu-id="e1c1c-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e1c1c-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e1c1c-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1c1c-144">-Confirm</span></span>
<span data-ttu-id="e1c1c-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c1c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c1c-146">-WhatIf</span></span>
<span data-ttu-id="e1c1c-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1c1c-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c1c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c1c-149">CommonParameters</span></span>
<span data-ttu-id="e1c1c-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c1c-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c1c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c1c-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1c1c-152">INPUTS</span></span>

### <span data-ttu-id="e1c1c-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e1c1c-153">None</span></span>
<span data-ttu-id="e1c1c-154">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e1c1c-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1c1c-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1c1c-155">OUTPUTS</span></span>

### <span data-ttu-id="e1c1c-156">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="e1c1c-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="e1c1c-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1c1c-157">NOTES</span></span>

## <span data-ttu-id="e1c1c-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1c1c-158">RELATED LINKS</span></span>

