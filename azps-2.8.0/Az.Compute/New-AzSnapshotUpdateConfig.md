---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: d2c029b75f5c451a2254b0dcf6b90c907148f8cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752841"
---
# <span data-ttu-id="876bd-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="876bd-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="876bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876bd-102">SYNOPSIS</span></span>
<span data-ttu-id="876bd-103">Yapılandırılabilir bir anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="876bd-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="876bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="876bd-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="876bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="876bd-105">DESCRIPTION</span></span>
<span data-ttu-id="876bd-106">**Yeni-AzSnapshotUpdateConfig** cmdlet 'i yapılandırılabilir bir anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="876bd-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="876bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="876bd-107">EXAMPLES</span></span>

### <span data-ttu-id="876bd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="876bd-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="876bd-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir boş anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="876bd-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="876bd-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="876bd-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="876bd-111">İkinci ve üçüncü komutlar, anlık görüntü güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="876bd-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="876bd-112">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="876bd-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="876bd-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="876bd-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="876bd-114">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="876bd-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="876bd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="876bd-115">PARAMETERS</span></span>

### <span data-ttu-id="876bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876bd-116">-DefaultProfile</span></span>
<span data-ttu-id="876bd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="876bd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876bd-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="876bd-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="876bd-119">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="876bd-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="876bd-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="876bd-120">-DiskSizeGB</span></span>
<span data-ttu-id="876bd-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="876bd-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="876bd-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="876bd-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="876bd-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="876bd-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="876bd-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="876bd-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="876bd-125">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="876bd-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="876bd-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="876bd-126">-OsType</span></span>
<span data-ttu-id="876bd-127">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="876bd-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="876bd-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="876bd-128">-SkuName</span></span>
<span data-ttu-id="876bd-129">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="876bd-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="876bd-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="876bd-130">-Tag</span></span>
<span data-ttu-id="876bd-131">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="876bd-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="876bd-132">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="876bd-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="876bd-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="876bd-133">-Confirm</span></span>
<span data-ttu-id="876bd-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="876bd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="876bd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="876bd-135">-WhatIf</span></span>
<span data-ttu-id="876bd-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="876bd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="876bd-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="876bd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="876bd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876bd-138">CommonParameters</span></span>
<span data-ttu-id="876bd-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="876bd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876bd-140">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="876bd-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876bd-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="876bd-141">INPUTS</span></span>

### <span data-ttu-id="876bd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="876bd-142">System.String</span></span>

### <span data-ttu-id="876bd-143">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="876bd-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="876bd-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="876bd-144">System.Int32</span></span>

### <span data-ttu-id="876bd-145">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="876bd-145">System.Collections.Hashtable</span></span>

### <span data-ttu-id="876bd-146">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="876bd-146">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="876bd-147">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="876bd-147">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="876bd-148">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="876bd-148">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="876bd-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="876bd-149">OUTPUTS</span></span>

### <span data-ttu-id="876bd-150">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="876bd-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="876bd-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="876bd-151">NOTES</span></span>

## <span data-ttu-id="876bd-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="876bd-152">RELATED LINKS</span></span>
