---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 70ee169903ca70b539e8eda2043ffcd0fd2928c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595009"
---
# <span data-ttu-id="ccff0-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ccff0-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="ccff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccff0-102">SYNOPSIS</span></span>
<span data-ttu-id="ccff0-103">Yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccff0-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccff0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccff0-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccff0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccff0-105">DESCRIPTION</span></span>
<span data-ttu-id="ccff0-106">**Yeni-AzureRmDiskConfig** cmdlet 'i, yapılandırılabilir bir disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccff0-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="ccff0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccff0-107">EXAMPLES</span></span>

### <span data-ttu-id="ccff0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ccff0-108">Example 1</span></span>
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

<span data-ttu-id="ccff0-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccff0-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ccff0-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="ccff0-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ccff0-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ccff0-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="ccff0-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccff0-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ccff0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccff0-113">PARAMETERS</span></span>

### <span data-ttu-id="ccff0-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="ccff0-114">-CreateOption</span></span>
<span data-ttu-id="ccff0-115">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="ccff0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccff0-116">-DefaultProfile</span></span>
<span data-ttu-id="ccff0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccff0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccff0-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ccff0-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="ccff0-119">Diskteki disk şifrelemesi anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="ccff0-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ccff0-120">-DiskSizeGB</span></span>
<span data-ttu-id="ccff0-121">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ccff0-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ccff0-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ccff0-123">Şifreleme ayarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ccff0-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ccff0-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="ccff0-124">-ImageReference</span></span>
<span data-ttu-id="ccff0-125">Diskteki resim başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="ccff0-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ccff0-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="ccff0-127">Bir diskte anahtar şifreleme anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="ccff0-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="ccff0-128">-Location</span></span>
<span data-ttu-id="ccff0-129">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-129">Specifies a location.</span></span>

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

### <span data-ttu-id="ccff0-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="ccff0-130">-OsType</span></span>
<span data-ttu-id="ccff0-131">İşletim sistemi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ccff0-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ccff0-132">-SkuName</span></span>
<span data-ttu-id="ccff0-133">Depolama hesabının SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="ccff0-134">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="ccff0-134">-SourceResourceId</span></span>
<span data-ttu-id="ccff0-135">Kaynak kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="ccff0-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ccff0-136">-SourceUri</span></span>
<span data-ttu-id="ccff0-137">Kaynak URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="ccff0-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="ccff0-138">-StorageAccountId</span></span>
<span data-ttu-id="ccff0-139">Depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="ccff0-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ccff0-140">-Tag</span></span>
<span data-ttu-id="ccff0-141">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="ccff0-142">-Bölge</span><span class="sxs-lookup"><span data-stu-id="ccff0-142">-Zone</span></span>
<span data-ttu-id="ccff0-143">Diskin mantıksal bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-143">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccff0-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="ccff0-144">-Confirm</span></span>
<span data-ttu-id="ccff0-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ccff0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccff0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccff0-146">-WhatIf</span></span>
<span data-ttu-id="ccff0-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccff0-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccff0-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ccff0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccff0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccff0-149">CommonParameters</span></span>
<span data-ttu-id="ccff0-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccff0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccff0-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccff0-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccff0-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccff0-152">INPUTS</span></span>

### <span data-ttu-id="ccff0-153">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ccff0-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="ccff0-154">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Koleksiyonlar. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ccff0-154">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ccff0-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccff0-155">OUTPUTS</span></span>

### <span data-ttu-id="ccff0-156">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="ccff0-156">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="ccff0-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccff0-157">NOTES</span></span>

## <span data-ttu-id="ccff0-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccff0-158">RELATED LINKS</span></span>

