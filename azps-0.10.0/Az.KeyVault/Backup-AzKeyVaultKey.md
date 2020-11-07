---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: d5fce3a4c70593b9478c0efa8afef29021797bb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935809"
---
# <span data-ttu-id="b3db2-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3db2-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="b3db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3db2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3db2-103">Anahtar kasasındaki bir anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="b3db2-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="b3db2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3db2-104">SYNTAX</span></span>

### <span data-ttu-id="b3db2-105">Byanahtaradı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3db2-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3db2-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="b3db2-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3db2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3db2-107">DESCRIPTION</span></span>
<span data-ttu-id="b3db2-108">**Backup-Azanahtarvaultkey** cmdlet 'i, anahtarı indirip bir dosyaya depolayarak bir Anahtar Kasası 'nda belirtilen anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="b3db2-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="b3db2-109">Anahtarın birden çok sürümü varsa, tüm sürümler yedeğe dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="b3db2-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="b3db2-110">İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b3db2-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="b3db2-111">Yedeklenmiş bir anahtarı, yedeklediğiniz abonelikteki herhangi bir anahtar kasaya geri yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3db2-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="b3db2-112">Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b3db2-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="b3db2-113">Anahtarınızın bir kopyasını, anahtar kasasındaki anahtarınızı yanlışlıkla silmeniz durumunda çevrimdışı bir kopya olacak şekilde sağlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="b3db2-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="b3db2-114">Anahtar Kasası kullanarak bir anahtar oluşturdunuz ve şimdi anahtarı başka bir Azure bölgesine kopyalamak istiyorsunuz; böylece bu uygulamayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3db2-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="b3db2-115">**Yedekleme-Azanahtarvaultkey** cmdlet 'ini kullanarak anahtarı şifreli biçimde alın ve Restore-AzKeyVaultKey cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.</span><span class="sxs-lookup"><span data-stu-id="b3db2-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="b3db2-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3db2-116">EXAMPLES</span></span>

### <span data-ttu-id="b3db2-117">Örnek 1: otomatik olarak oluşturulan bir dosya adıyla anahtarı yedekleme</span><span class="sxs-lookup"><span data-stu-id="b3db2-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="b3db2-118">Bu komut Mykeykasası adındaki anahtar kasasından MyKey adlı anahtarı alır ve bu anahtarın bir yedeğini sizin için otomatik olarak adlandırılmış bir dosyaya kaydeder ve dosya adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b3db2-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="b3db2-119">Örnek 2: anahtarı belirtilen dosya adına yedekleme</span><span class="sxs-lookup"><span data-stu-id="b3db2-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="b3db2-120">Bu komut Mykeykasası adındaki anahtar vaultmykey adındaki anahtarı alır ve bu anahtarın yedeğini Backup. blob adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b3db2-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="b3db2-121">Örnek 3: önceden alınan bir anahtarı belirtilen dosya adına yedekleyin, hedef dosyanın üzerine sormadan dosyaya yazılır.</span><span class="sxs-lookup"><span data-stu-id="b3db2-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="b3db2-122">Bu komut $key adlı anahtarın bir yedeğini oluşturur. $Key adlı kasada ad. VaultName, yedek. blob adlı bir dosyaya, zaten varsa dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="b3db2-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="b3db2-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3db2-123">PARAMETERS</span></span>

### <span data-ttu-id="b3db2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3db2-124">-DefaultProfile</span></span>
<span data-ttu-id="b3db2-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3db2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3db2-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b3db2-126">-Force</span></span>
<span data-ttu-id="b3db2-127">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="b3db2-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="b3db2-128">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="b3db2-128">-Key</span></span>
<span data-ttu-id="b3db2-129">Yedeklenecek olan daha önce alınan bir anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3db2-129">Specifies a previously retrieved key which is to be backed up.</span></span>

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

### <span data-ttu-id="b3db2-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3db2-130">-Name</span></span>
<span data-ttu-id="b3db2-131">Yedekleme için anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3db2-131">Specifies the name of the key to back up.</span></span>

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

### <span data-ttu-id="b3db2-132">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="b3db2-132">-OutputFile</span></span>
<span data-ttu-id="b3db2-133">Yedekleme bloonun depolandığı çıkış dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3db2-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="b3db2-134">Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir dosya adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3db2-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="b3db2-135">Var olan bir çıkış dosyasının adını belirtirseniz, işlem tamamlanmıştır ve yedekleme dosyasının zaten var olduğunu belirten bir hata iletisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3db2-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="b3db2-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b3db2-136">-VaultName</span></span>
<span data-ttu-id="b3db2-137">Yedekleme anahtarını içeren Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3db2-137">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="b3db2-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3db2-138">-Confirm</span></span>
<span data-ttu-id="b3db2-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3db2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3db2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3db2-140">-WhatIf</span></span>
<span data-ttu-id="b3db2-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3db2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3db2-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3db2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3db2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3db2-143">CommonParameters</span></span>
<span data-ttu-id="b3db2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3db2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3db2-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3db2-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3db2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3db2-146">INPUTS</span></span>

### <span data-ttu-id="b3db2-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b3db2-147">None</span></span>
<span data-ttu-id="b3db2-148">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b3db2-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3db2-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3db2-149">OUTPUTS</span></span>

### <span data-ttu-id="b3db2-150">Dizisi</span><span class="sxs-lookup"><span data-stu-id="b3db2-150">String</span></span>
<span data-ttu-id="b3db2-151">Cmdlet, anahtarın yedeğini içeren çıkış dosyasının yolunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3db2-151">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="b3db2-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3db2-152">NOTES</span></span>

## <span data-ttu-id="b3db2-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3db2-153">RELATED LINKS</span></span>

[<span data-ttu-id="b3db2-154">Add-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="b3db2-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="b3db2-155">Get-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="b3db2-155">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="b3db2-156">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3db2-156">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="b3db2-157">Restore-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="b3db2-157">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

