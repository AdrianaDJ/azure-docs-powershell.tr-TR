---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 1afd1631e398b5726a8e1002b6739fc7ac9b67a8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936964"
---
# <span data-ttu-id="00908-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="00908-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="00908-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00908-102">SYNOPSIS</span></span>
<span data-ttu-id="00908-103">Yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00908-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="00908-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00908-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00908-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00908-105">DESCRIPTION</span></span>
<span data-ttu-id="00908-106">**Yeni-AzSnapshotConfig** cmdlet 'i yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00908-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="00908-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00908-107">EXAMPLES</span></span>

### <span data-ttu-id="00908-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="00908-108">Example 1</span></span>
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

<span data-ttu-id="00908-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00908-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="00908-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="00908-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="00908-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="00908-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="00908-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00908-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="00908-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00908-113">PARAMETERS</span></span>

### <span data-ttu-id="00908-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="00908-114">-CreateOption</span></span>
<span data-ttu-id="00908-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="00908-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="00908-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00908-116">-DefaultProfile</span></span>
<span data-ttu-id="00908-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00908-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00908-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="00908-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="00908-119">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="00908-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="00908-120">-DiskSizeGB</span></span>
<span data-ttu-id="00908-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="00908-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="00908-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="00908-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="00908-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="00908-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="00908-124">-ImageReference</span></span>
<span data-ttu-id="00908-125">Anlık görüntüdeki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="00908-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="00908-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="00908-127">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="00908-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="00908-128">-Location</span></span>
<span data-ttu-id="00908-129">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-129">Specifies a location.</span></span>

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

### <span data-ttu-id="00908-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="00908-130">-OsType</span></span>
<span data-ttu-id="00908-131">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="00908-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="00908-132">-SkuName</span></span>
<span data-ttu-id="00908-133">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="00908-134">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="00908-134">-SourceResourceId</span></span>
<span data-ttu-id="00908-135">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="00908-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="00908-136">-SourceUri</span></span>
<span data-ttu-id="00908-137">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="00908-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="00908-138">-StorageAccountId</span></span>
<span data-ttu-id="00908-139">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="00908-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="00908-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="00908-140">-Tag</span></span>
<span data-ttu-id="00908-141">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="00908-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="00908-142">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="00908-142">For example:</span></span>

<span data-ttu-id="00908-143">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="00908-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="00908-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="00908-144">-Confirm</span></span>
<span data-ttu-id="00908-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00908-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00908-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00908-146">-WhatIf</span></span>
<span data-ttu-id="00908-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00908-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00908-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00908-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00908-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00908-149">CommonParameters</span></span>
<span data-ttu-id="00908-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00908-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00908-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00908-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00908-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00908-152">INPUTS</span></span>

### <span data-ttu-id="00908-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="00908-153">None</span></span>
<span data-ttu-id="00908-154">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="00908-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00908-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00908-155">OUTPUTS</span></span>

### <span data-ttu-id="00908-156">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="00908-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="00908-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00908-157">NOTES</span></span>

## <span data-ttu-id="00908-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00908-158">RELATED LINKS</span></span>

