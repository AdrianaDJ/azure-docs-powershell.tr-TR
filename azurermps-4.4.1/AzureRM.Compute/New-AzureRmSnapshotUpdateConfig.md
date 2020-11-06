---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 00519ec40e4f173c7ecfbb37189835711184f2e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594787"
---
# <span data-ttu-id="f52c1-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f52c1-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="f52c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f52c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f52c1-103">Yapılandırılabilir bir anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f52c1-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f52c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f52c1-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f52c1-105">DESCRIPTION</span></span>
<span data-ttu-id="f52c1-106">**Yeni-AzureRmSnapshotUpdateConfig** cmdlet 'i, yapılandırılabilir bir anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f52c1-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="f52c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f52c1-107">EXAMPLES</span></span>

### <span data-ttu-id="f52c1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f52c1-108">Example 1</span></span>
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

<span data-ttu-id="f52c1-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir boş anlık görüntü güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f52c1-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="f52c1-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="f52c1-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="f52c1-111">İkinci ve üçüncü komutlar, anlık görüntü güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f52c1-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="f52c1-112">Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f52c1-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f52c1-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="f52c1-114">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü 10 GB disk boyutuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="f52c1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f52c1-115">PARAMETERS</span></span>

### <span data-ttu-id="f52c1-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f52c1-116">-CreateOption</span></span>
<span data-ttu-id="f52c1-117">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden anlık görüntü oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya mevcut bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-117">Specifies whether this cmdlet creates a snapshot in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="f52c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52c1-118">-DefaultProfile</span></span>
<span data-ttu-id="f52c1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f52c1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f52c1-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f52c1-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="f52c1-121">Anlık görüntüdeki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-121">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="f52c1-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f52c1-122">-DiskSizeGB</span></span>
<span data-ttu-id="f52c1-123">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="f52c1-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="f52c1-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="f52c1-125">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f52c1-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="f52c1-126">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="f52c1-126">-ImageReference</span></span>
<span data-ttu-id="f52c1-127">Anlık görüntüdeki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-127">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="f52c1-128">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f52c1-128">-KeyEncryptionKey</span></span>
<span data-ttu-id="f52c1-129">Anlık görüntüdeki anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-129">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="f52c1-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="f52c1-130">-OsType</span></span>
<span data-ttu-id="f52c1-131">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="f52c1-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f52c1-132">-SkuName</span></span>
<span data-ttu-id="f52c1-133">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="f52c1-134">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="f52c1-134">-SourceResourceId</span></span>
<span data-ttu-id="f52c1-135">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="f52c1-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="f52c1-136">-SourceUri</span></span>
<span data-ttu-id="f52c1-137">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="f52c1-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="f52c1-138">-StorageAccountId</span></span>
<span data-ttu-id="f52c1-139">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="f52c1-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f52c1-140">-Tag</span></span>
<span data-ttu-id="f52c1-141">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="f52c1-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="f52c1-142">-Confirm</span></span>
<span data-ttu-id="f52c1-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f52c1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f52c1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52c1-144">-WhatIf</span></span>
<span data-ttu-id="f52c1-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f52c1-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f52c1-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f52c1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f52c1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52c1-147">CommonParameters</span></span>
<span data-ttu-id="f52c1-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f52c1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52c1-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52c1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52c1-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f52c1-150">INPUTS</span></span>

### <span data-ttu-id="f52c1-151">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f52c1-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="f52c1-152">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Koleksiyonlar. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f52c1-152">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="f52c1-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f52c1-153">OUTPUTS</span></span>

### <span data-ttu-id="f52c1-154">Microsoft. Azure. Management. COMPUTE. modeller. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="f52c1-154">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="f52c1-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f52c1-155">NOTES</span></span>

## <span data-ttu-id="f52c1-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f52c1-156">RELATED LINKS</span></span>

