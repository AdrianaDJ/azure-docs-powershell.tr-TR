---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: c346cebbc14a25b2afa8047deea3578ab8330d87
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936972"
---
# <span data-ttu-id="b3117-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="b3117-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="b3117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3117-102">SYNOPSIS</span></span>
<span data-ttu-id="b3117-103">Yapılandırılabilir bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3117-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="b3117-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3117-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3117-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3117-105">DESCRIPTION</span></span>
<span data-ttu-id="b3117-106">**New-AzDiskUpdateConfig** cmdlet 'i yapılandırılabilir bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3117-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="b3117-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3117-107">EXAMPLES</span></span>

### <span data-ttu-id="b3117-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b3117-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="b3117-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3117-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="b3117-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="b3117-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="b3117-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b3117-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="b3117-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b3117-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b3117-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b3117-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="b3117-114">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı mevcut diski 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b3117-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b3117-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3117-115">PARAMETERS</span></span>

### <span data-ttu-id="b3117-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3117-116">-DefaultProfile</span></span>
<span data-ttu-id="b3117-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3117-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3117-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b3117-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="b3117-119">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3117-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="b3117-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b3117-120">-DiskSizeGB</span></span>
<span data-ttu-id="b3117-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3117-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b3117-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="b3117-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b3117-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="b3117-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="b3117-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b3117-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="b3117-125">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3117-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="b3117-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="b3117-126">-OsType</span></span>
<span data-ttu-id="b3117-127">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3117-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="b3117-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b3117-128">-SkuName</span></span>
<span data-ttu-id="b3117-129">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3117-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="b3117-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b3117-130">-Tag</span></span>
<span data-ttu-id="b3117-131">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="b3117-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b3117-132">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="b3117-132">For example:</span></span>

<span data-ttu-id="b3117-133">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="b3117-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b3117-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3117-134">-Confirm</span></span>
<span data-ttu-id="b3117-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3117-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3117-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3117-136">-WhatIf</span></span>
<span data-ttu-id="b3117-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3117-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3117-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3117-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3117-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3117-139">CommonParameters</span></span>
<span data-ttu-id="b3117-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3117-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3117-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3117-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3117-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3117-142">INPUTS</span></span>

### <span data-ttu-id="b3117-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b3117-143">None</span></span>
<span data-ttu-id="b3117-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b3117-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3117-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3117-145">OUTPUTS</span></span>

### <span data-ttu-id="b3117-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsReference</span><span class="sxs-lookup"><span data-stu-id="b3117-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="b3117-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3117-147">NOTES</span></span>

## <span data-ttu-id="b3117-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3117-148">RELATED LINKS</span></span>

