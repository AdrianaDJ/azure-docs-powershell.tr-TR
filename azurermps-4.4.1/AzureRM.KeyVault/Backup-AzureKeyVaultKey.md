---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://go.microsoft.com/fwlink/?LinkId=690296
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: f6d6b362a93897dc854170b8cbbbfd228b305abc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765171"
---
# <span data-ttu-id="c2504-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2504-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="c2504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2504-102">SYNOPSIS</span></span>
<span data-ttu-id="c2504-103">Anahtar kasasındaki bir anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="c2504-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2504-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2504-104">SYNTAX</span></span>

### <span data-ttu-id="c2504-105">Byanahtaradı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2504-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2504-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="c2504-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2504-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2504-107">DESCRIPTION</span></span>
<span data-ttu-id="c2504-108">**Backup-AzureKeyVaultKey** cmdlet 'i, bir Anahtar Kasası içinde, dosyayı indirip bir dosyaya depolayarak belirtilen anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="c2504-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="c2504-109">Anahtarın birden çok sürümü varsa, tüm sürümler yedeğe dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="c2504-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="c2504-110">İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="c2504-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="c2504-111">Yedeklenmiş bir anahtarı, yedeklediğiniz abonelikteki herhangi bir anahtar kasaya geri yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2504-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="c2504-112">Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c2504-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="c2504-113">Anahtarınızın bir kopyasını, anahtar kasasındaki anahtarınızı yanlışlıkla silmeniz durumunda çevrimdışı bir kopya olacak şekilde sağlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="c2504-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="c2504-114">Anahtar Kasası kullanarak bir anahtar oluşturdunuz ve şimdi anahtarı başka bir Azure bölgesine kopyalamak istiyorsunuz; böylece bu uygulamayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2504-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="c2504-115">**Backup-AzureKeyVaultKey** cmdlet 'ini kullanarak anahtarı şifreli biçimde alın ve Restore-AzureKeyVaultKey cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.</span><span class="sxs-lookup"><span data-stu-id="c2504-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="c2504-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2504-116">EXAMPLES</span></span>

### <span data-ttu-id="c2504-117">Örnek 1: otomatik olarak oluşturulan bir dosya adıyla anahtarı yedekleme</span><span class="sxs-lookup"><span data-stu-id="c2504-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="c2504-118">Bu komut Mykeykasası adındaki anahtar kasasından MyKey adlı anahtarı alır ve bu anahtarın bir yedeğini sizin için otomatik olarak adlandırılmış bir dosyaya kaydeder ve dosya adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c2504-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="c2504-119">Örnek 2: anahtarı belirtilen dosya adına yedekleme</span><span class="sxs-lookup"><span data-stu-id="c2504-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="c2504-120">Bu komut Mykeykasası adındaki anahtar vaultmykey adındaki anahtarı alır ve bu anahtarın yedeğini Backup. blob adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c2504-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="c2504-121">Örnek 3: önceden alınan bir anahtarı belirtilen dosya adına yedekleyin, hedef dosyanın üzerine sormadan dosyaya yazılır.</span><span class="sxs-lookup"><span data-stu-id="c2504-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="c2504-122">Bu komut $key adlı anahtarın bir yedeğini oluşturur. $Key adlı kasada ad. VaultName, yedek. blob adlı bir dosyaya, zaten varsa dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="c2504-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="c2504-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2504-123">PARAMETERS</span></span>

### <span data-ttu-id="c2504-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c2504-124">-Force</span></span>
<span data-ttu-id="c2504-125">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="c2504-125">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2504-126">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="c2504-126">-Key</span></span>
<span data-ttu-id="c2504-127">Yedeklenecek olan daha önce alınan bir anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2504-127">Specifies a previously retrieved key which is to be backed up.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyBundle
Parameter Sets: ByKey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2504-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2504-128">-Name</span></span>
<span data-ttu-id="c2504-129">Yedekleme için anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2504-129">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2504-130">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="c2504-130">-OutputFile</span></span>
<span data-ttu-id="c2504-131">Yedekleme bloonun depolandığı çıkış dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2504-131">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="c2504-132">Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir dosya adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2504-132">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="c2504-133">Var olan bir çıkış dosyasının adını belirtirseniz, işlem tamamlanmıştır ve yedekleme dosyasının zaten var olduğunu belirten bir hata iletisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c2504-133">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="c2504-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c2504-134">-VaultName</span></span>
<span data-ttu-id="c2504-135">Yedekleme anahtarını içeren Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2504-135">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2504-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2504-136">-Confirm</span></span>
<span data-ttu-id="c2504-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2504-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2504-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2504-138">-WhatIf</span></span>
<span data-ttu-id="c2504-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2504-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2504-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2504-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2504-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2504-141">-DefaultProfile</span></span>
<span data-ttu-id="c2504-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2504-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2504-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2504-143">CommonParameters</span></span>
<span data-ttu-id="c2504-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2504-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2504-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2504-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2504-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2504-146">INPUTS</span></span>

## <span data-ttu-id="c2504-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2504-147">OUTPUTS</span></span>

### <span data-ttu-id="c2504-148">Dizisi</span><span class="sxs-lookup"><span data-stu-id="c2504-148">String</span></span>
<span data-ttu-id="c2504-149">Cmdlet, anahtarın yedeğini içeren çıkış dosyasının yolunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="c2504-149">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="c2504-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2504-150">NOTES</span></span>

## <span data-ttu-id="c2504-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2504-151">RELATED LINKS</span></span>

[<span data-ttu-id="c2504-152">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2504-152">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="c2504-153">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2504-153">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="c2504-154">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2504-154">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="c2504-155">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c2504-155">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

