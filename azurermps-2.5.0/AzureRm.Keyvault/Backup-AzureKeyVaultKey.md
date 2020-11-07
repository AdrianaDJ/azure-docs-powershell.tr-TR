---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: e2c169109727fb57f8d044d17de5f15a7e2835f6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938847"
---
# <span data-ttu-id="0f400-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f400-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="0f400-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f400-102">SYNOPSIS</span></span>
<span data-ttu-id="0f400-103">Anahtar kasasındaki bir anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="0f400-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f400-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f400-104">SYNTAX</span></span>

### <span data-ttu-id="0f400-105">Byanahtaradı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f400-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f400-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="0f400-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f400-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f400-107">DESCRIPTION</span></span>
<span data-ttu-id="0f400-108">**Backup-AzureKeyVaultKey** cmdlet 'i, bir Anahtar Kasası içinde, dosyayı indirip bir dosyaya depolayarak belirtilen anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="0f400-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="0f400-109">Anahtarın birden çok sürümü varsa, tüm sürümler yedeğe dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="0f400-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="0f400-110">İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="0f400-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="0f400-111">Yedeklenmiş bir anahtarı, yedeklediğiniz abonelikteki herhangi bir anahtar kasaya geri yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f400-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="0f400-112">Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0f400-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="0f400-113">Anahtarınızın bir kopyasını, anahtar kasasındaki anahtarınızı yanlışlıkla silmeniz durumunda çevrimdışı bir kopya olacak şekilde sağlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="0f400-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="0f400-114">Anahtar Kasası kullanarak bir anahtar oluşturdunuz ve şimdi anahtarı başka bir Azure bölgesine kopyalamak istiyorsunuz; böylece bu uygulamayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f400-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="0f400-115">**Backup-AzureKeyVaultKey** cmdlet 'ini kullanarak anahtarı şifreli biçimde alın ve Restore-AzureKeyVaultKey cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.</span><span class="sxs-lookup"><span data-stu-id="0f400-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="0f400-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f400-116">EXAMPLES</span></span>

### <span data-ttu-id="0f400-117">Örnek 1: otomatik olarak oluşturulan bir dosya adıyla anahtarı yedekleme</span><span class="sxs-lookup"><span data-stu-id="0f400-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="0f400-118">Bu komut Mykeykasası adındaki anahtar kasasından MyKey adlı anahtarı alır ve bu anahtarın bir yedeğini sizin için otomatik olarak adlandırılmış bir dosyaya kaydeder ve dosya adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="0f400-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="0f400-119">Örnek 2: anahtarı belirtilen dosya adına yedekleme</span><span class="sxs-lookup"><span data-stu-id="0f400-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="0f400-120">Bu komut Mykeykasası adındaki anahtar vaultmykey adındaki anahtarı alır ve bu anahtarın yedeğini Backup. blob adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0f400-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="0f400-121">Örnek 3: önceden alınan bir anahtarı belirtilen dosya adına yedekleyin, hedef dosyanın üzerine sormadan dosyaya yazılır.</span><span class="sxs-lookup"><span data-stu-id="0f400-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="0f400-122">Bu komut $key adlı anahtarın bir yedeğini oluşturur. $Key adlı kasada ad. VaultName, yedek. blob adlı bir dosyaya, zaten varsa dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="0f400-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="0f400-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f400-123">PARAMETERS</span></span>

### <span data-ttu-id="0f400-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f400-124">-DefaultProfile</span></span>
<span data-ttu-id="0f400-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0f400-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f400-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0f400-126">-Force</span></span>
<span data-ttu-id="0f400-127">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="0f400-127">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f400-128">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="0f400-128">-Key</span></span>
<span data-ttu-id="0f400-129">Yedeklenecek olan daha önce alınan bir anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f400-129">Specifies a previously retrieved key which is to be backed up.</span></span>

```yaml
Type: KeyBundle
Parameter Sets: ByKey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f400-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f400-130">-Name</span></span>
<span data-ttu-id="0f400-131">Yedekleme için anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f400-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f400-132">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="0f400-132">-OutputFile</span></span>
<span data-ttu-id="0f400-133">Yedekleme bloonun depolandığı çıkış dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f400-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="0f400-134">Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir dosya adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f400-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="0f400-135">Var olan bir çıkış dosyasının adını belirtirseniz, işlem tamamlanmıştır ve yedekleme dosyasının zaten var olduğunu belirten bir hata iletisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f400-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f400-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0f400-136">-VaultName</span></span>
<span data-ttu-id="0f400-137">Yedekleme anahtarını içeren Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f400-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f400-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f400-138">-Confirm</span></span>
<span data-ttu-id="0f400-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f400-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f400-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f400-140">-WhatIf</span></span>
<span data-ttu-id="0f400-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f400-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f400-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f400-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f400-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f400-143">CommonParameters</span></span>
<span data-ttu-id="0f400-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f400-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f400-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f400-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f400-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f400-146">INPUTS</span></span>

## <span data-ttu-id="0f400-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f400-147">OUTPUTS</span></span>

### <span data-ttu-id="0f400-148">Dizisi</span><span class="sxs-lookup"><span data-stu-id="0f400-148">String</span></span>
<span data-ttu-id="0f400-149">Cmdlet, anahtarın yedeğini içeren çıkış dosyasının yolunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f400-149">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="0f400-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f400-150">NOTES</span></span>

## <span data-ttu-id="0f400-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f400-151">RELATED LINKS</span></span>

[<span data-ttu-id="0f400-152">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f400-152">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="0f400-153">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f400-153">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="0f400-154">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f400-154">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="0f400-155">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f400-155">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

