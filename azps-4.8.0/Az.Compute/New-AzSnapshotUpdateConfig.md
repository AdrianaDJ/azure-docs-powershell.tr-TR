---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110029"
---
# <span data-ttu-id="4be8e-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="4be8e-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="4be8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4be8e-102">SYNOPSIS</span></span>
<span data-ttu-id="4be8e-103">Yapılandırılabilir bir anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4be8e-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="4be8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4be8e-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be8e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4be8e-105">DESCRIPTION</span></span>
<span data-ttu-id="4be8e-106">**Yeni-AzSnapshotUpdateConfig** cmdlet 'i yapılandırılabilir bir anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4be8e-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="4be8e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4be8e-107">EXAMPLES</span></span>

### <span data-ttu-id="4be8e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4be8e-108">Example 1</span></span>
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

<span data-ttu-id="4be8e-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir boş anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4be8e-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="4be8e-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="4be8e-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="4be8e-111">İkinci ve üçüncü komutlar, anlık görüntü güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4be8e-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="4be8e-112">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="4be8e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4be8e-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="4be8e-114">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="4be8e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4be8e-115">PARAMETERS</span></span>

### <span data-ttu-id="4be8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be8e-116">-DefaultProfile</span></span>
<span data-ttu-id="4be8e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4be8e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4be8e-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4be8e-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="4be8e-119">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="4be8e-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="4be8e-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="4be8e-121">Rest 'de şifrelemeyi etkinleştirmek için kullanılacak disk şifrelemesi kümesi kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8e-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="4be8e-122">-DiskSizeGB</span></span>
<span data-ttu-id="4be8e-123">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="4be8e-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="4be8e-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="4be8e-125">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="4be8e-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="4be8e-126">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="4be8e-126">-EncryptionType</span></span>
<span data-ttu-id="4be8e-127">Diskin verilerini şifrelemek için kullanılan anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="4be8e-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="4be8e-128">Kullanılabilir değerler şunlardır: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="4be8e-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8e-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4be8e-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="4be8e-130">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="4be8e-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="4be8e-131">-OsType</span></span>
<span data-ttu-id="4be8e-132">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="4be8e-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4be8e-133">-SkuName</span></span>
<span data-ttu-id="4be8e-134">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="4be8e-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4be8e-135">-Tag</span></span>
<span data-ttu-id="4be8e-136">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4be8e-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4be8e-137">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4be8e-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4be8e-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="4be8e-138">-Confirm</span></span>
<span data-ttu-id="4be8e-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4be8e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be8e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be8e-140">-WhatIf</span></span>
<span data-ttu-id="4be8e-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4be8e-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4be8e-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4be8e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be8e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be8e-143">CommonParameters</span></span>
<span data-ttu-id="4be8e-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4be8e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be8e-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4be8e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be8e-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4be8e-146">INPUTS</span></span>

### <span data-ttu-id="4be8e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4be8e-147">System.String</span></span>

### <span data-ttu-id="4be8e-148">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4be8e-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="4be8e-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4be8e-149">System.Int32</span></span>

### <span data-ttu-id="4be8e-150">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4be8e-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4be8e-151">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="4be8e-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4be8e-152">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="4be8e-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="4be8e-153">Microsoft. Azure. Management. COMPUTE. modeller. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="4be8e-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="4be8e-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4be8e-154">OUTPUTS</span></span>

### <span data-ttu-id="4be8e-155">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="4be8e-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="4be8e-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4be8e-156">NOTES</span></span>

## <span data-ttu-id="4be8e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4be8e-157">RELATED LINKS</span></span>
