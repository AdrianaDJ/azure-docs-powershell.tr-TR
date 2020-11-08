---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotupdateconfig
schema: 2.0.0
ms.openlocfilehash: 033b183c763be266b29aadf47a57e760e2432452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939791"
---
# <span data-ttu-id="1e6dd-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="1e6dd-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="1e6dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6dd-103">Yapılandırılabilir bir anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e6dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e6dd-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e6dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="1e6dd-106">**Yeni-AzureRmSnapshotUpdateConfig** cmdlet 'i, yapılandırılabilir bir anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="1e6dd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e6dd-107">EXAMPLES</span></span>

### <span data-ttu-id="1e6dd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e6dd-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="1e6dd-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir boş anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="1e6dd-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="1e6dd-111">İkinci ve üçüncü komutlar, anlık görüntü güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="1e6dd-112">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1e6dd-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1e6dd-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="1e6dd-114">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="1e6dd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e6dd-115">PARAMETERS</span></span>

### <span data-ttu-id="1e6dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6dd-116">-DefaultProfile</span></span>
<span data-ttu-id="1e6dd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e6dd-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1e6dd-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="1e6dd-119">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="1e6dd-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1e6dd-120">-DiskSizeGB</span></span>
<span data-ttu-id="1e6dd-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="1e6dd-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1e6dd-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="1e6dd-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="1e6dd-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1e6dd-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="1e6dd-125">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="1e6dd-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="1e6dd-126">-OsType</span></span>
<span data-ttu-id="1e6dd-127">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="1e6dd-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1e6dd-128">-SkuName</span></span>
<span data-ttu-id="1e6dd-129">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="1e6dd-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1e6dd-130">-Tag</span></span>
<span data-ttu-id="1e6dd-131">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1e6dd-132">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="1e6dd-132">For example:</span></span>

<span data-ttu-id="1e6dd-133">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1e6dd-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1e6dd-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e6dd-134">-Confirm</span></span>
<span data-ttu-id="1e6dd-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e6dd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e6dd-136">-WhatIf</span></span>
<span data-ttu-id="1e6dd-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e6dd-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e6dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6dd-139">CommonParameters</span></span>
<span data-ttu-id="1e6dd-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6dd-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6dd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6dd-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e6dd-142">INPUTS</span></span>

### <span data-ttu-id="1e6dd-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1e6dd-143">None</span></span>
<span data-ttu-id="1e6dd-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1e6dd-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e6dd-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e6dd-145">OUTPUTS</span></span>

### <span data-ttu-id="1e6dd-146">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="1e6dd-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="1e6dd-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e6dd-147">NOTES</span></span>

## <span data-ttu-id="1e6dd-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e6dd-148">RELATED LINKS</span></span>
