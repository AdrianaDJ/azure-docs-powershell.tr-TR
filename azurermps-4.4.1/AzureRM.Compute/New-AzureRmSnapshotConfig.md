---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: 032868a1dc1e183a2dd4adea31bbf693cdd7d1ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594791"
---
# <span data-ttu-id="07add-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="07add-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="07add-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07add-102">SYNOPSIS</span></span>
<span data-ttu-id="07add-103">Yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07add-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07add-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07add-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07add-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07add-105">DESCRIPTION</span></span>
<span data-ttu-id="07add-106">**Yeni-AzureRmSnapshotConfig** cmdlet 'i, yapılandırılabilir bir anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07add-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="07add-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07add-107">EXAMPLES</span></span>

### <span data-ttu-id="07add-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07add-108">Example 1</span></span>
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

<span data-ttu-id="07add-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07add-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="07add-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="07add-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="07add-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07add-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="07add-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07add-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="07add-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07add-113">PARAMETERS</span></span>

### <span data-ttu-id="07add-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="07add-114">-CreateOption</span></span>
<span data-ttu-id="07add-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="07add-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07add-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07add-116">-DefaultProfile</span></span>
<span data-ttu-id="07add-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07add-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07add-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="07add-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="07add-119">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="07add-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="07add-120">-DiskSizeGB</span></span>
<span data-ttu-id="07add-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07add-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="07add-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="07add-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="07add-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="07add-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="07add-124">-ImageReference</span></span>
<span data-ttu-id="07add-125">Anlık görüntüdeki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-125">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07add-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="07add-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="07add-127">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="07add-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="07add-128">-Location</span></span>
<span data-ttu-id="07add-129">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-129">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07add-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="07add-130">-OsType</span></span>
<span data-ttu-id="07add-131">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="07add-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="07add-132">-SkuName</span></span>
<span data-ttu-id="07add-133">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07add-134">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="07add-134">-SourceResourceId</span></span>
<span data-ttu-id="07add-135">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="07add-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="07add-136">-SourceUri</span></span>
<span data-ttu-id="07add-137">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="07add-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="07add-138">-StorageAccountId</span></span>
<span data-ttu-id="07add-139">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="07add-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="07add-140">-Tag</span></span>
<span data-ttu-id="07add-141">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07add-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07add-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="07add-142">-Confirm</span></span>
<span data-ttu-id="07add-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07add-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07add-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07add-144">-WhatIf</span></span>
<span data-ttu-id="07add-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07add-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07add-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07add-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07add-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07add-147">CommonParameters</span></span>
<span data-ttu-id="07add-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07add-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07add-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07add-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07add-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07add-150">INPUTS</span></span>

### <span data-ttu-id="07add-151">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="07add-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="07add-152">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Koleksiyonlar. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="07add-152">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="07add-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07add-153">OUTPUTS</span></span>

### <span data-ttu-id="07add-154">Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü</span><span class="sxs-lookup"><span data-stu-id="07add-154">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="07add-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07add-155">NOTES</span></span>

## <span data-ttu-id="07add-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07add-156">RELATED LINKS</span></span>

