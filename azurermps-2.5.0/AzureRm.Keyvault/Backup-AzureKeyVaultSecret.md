---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: cd83d61c64e4111faf7fc6149107e172d0cf0c9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938848"
---
# <span data-ttu-id="c4fd2-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4fd2-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="c4fd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fd2-103">Bir Anahtar Kasası içinde gizliliği yedekler.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4fd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4fd2-104">SYNTAX</span></span>

### <span data-ttu-id="c4fd2-105">BySecretName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4fd2-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fd2-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="c4fd2-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4fd2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4fd2-107">DESCRIPTION</span></span>
<span data-ttu-id="c4fd2-108">**Backup-AzureKeyVaultSecret** cmdlet 'i, bir Anahtar Kasası içinde belirtilen bir parolayı indirip dosyaya kaydederek yedekler.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="c4fd2-109">Gizlilik 'in birden çok sürümü varsa, tüm sürümler yedeğe dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="c4fd2-110">İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="c4fd2-111">Yedeklenmiş bir parolayı, yedeklediğiniz abonelikteki herhangi bir anahtar kasasına geri yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="c4fd2-112">Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c4fd2-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="c4fd2-113">Gizli bir kopyasını, anahtar kasasına yanlışlıkla silmeniz olasılığına karşı çevrimdışı bir kopya oluşturmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="c4fd2-114">Bir anahtar kasaya gizli eklediniz ve şimdi parolayı başka bir Azure bölgesine kopyalamak istiyorsunuz, böylece bu parolayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="c4fd2-115">Parolayı şifreli biçimde almak için Backup-AzureKeyVaultSecret cmdlet 'ini kullanın ve Restore-AzureKeyVaultSecret cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="c4fd2-116">(Bölgelerin aynı coğrafya 'ya ait olması gerektiğini unutmayın.)</span><span class="sxs-lookup"><span data-stu-id="c4fd2-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="c4fd2-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4fd2-117">EXAMPLES</span></span>

### <span data-ttu-id="c4fd2-118">Örnek 1: otomatik olarak oluşturulan bir dosya adıyla parolayı yedekleme</span><span class="sxs-lookup"><span data-stu-id="c4fd2-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="c4fd2-119">Bu komut Mykeykasası adlı anahtar kasasından MySecret adındaki parolayı alır ve bu gizli dosyanın bir yedeğini sizin için otomatik olarak adlandırılan bir dosyaya kaydeder ve dosya adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="c4fd2-120">Örnek 2: parolayı belirli bir dosya adına yedekleme</span><span class="sxs-lookup"><span data-stu-id="c4fd2-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="c4fd2-121">Bu komut Mykeykasası adındaki anahtar vaultmysecret adlı parolayı alır ve bu gizli dosyanın bir yedeğini Backup. blob adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="c4fd2-122">Örnek 3: daha önce belirli bir dosya adına alınan bir parolayı yedekleme</span><span class="sxs-lookup"><span data-stu-id="c4fd2-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="c4fd2-123">Bu komut, parolayı almak için $secret nesnenin kasa adını ve adını kullanır ve yedeklemesini Backup. blob adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="c4fd2-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4fd2-124">PARAMETERS</span></span>

### <span data-ttu-id="c4fd2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fd2-125">-DefaultProfile</span></span>
<span data-ttu-id="c4fd2-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c4fd2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4fd2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c4fd2-127">-Force</span></span>
<span data-ttu-id="c4fd2-128">Varsa, çıkış dosyasının üzerine yazmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd2-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4fd2-129">-Name</span></span>
<span data-ttu-id="c4fd2-130">Yedekleme için parola adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-130">Specifies the name of the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd2-131">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="c4fd2-131">-OutputFile</span></span>
<span data-ttu-id="c4fd2-132">Yedekleme bloonun depolandığı çıkış dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-132">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="c4fd2-133">Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir dosya adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-133">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="c4fd2-134">Var olan bir çıkış dosyasının adını belirtirseniz, işlem tamamlanmıştır ve yedekleme dosyasının zaten var olduğunu belirten bir hata iletisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-134">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="c4fd2-135">-Parola</span><span class="sxs-lookup"><span data-stu-id="c4fd2-135">-Secret</span></span>
<span data-ttu-id="c4fd2-136">Yedekleme işlemi için adı ve Kasası kullanılması gereken nesneyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-136">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd2-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c4fd2-137">-VaultName</span></span>
<span data-ttu-id="c4fd2-138">Yedekleme için parolayı içeren Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd2-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4fd2-139">-Confirm</span></span>
<span data-ttu-id="c4fd2-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4fd2-141">-WhatIf</span></span>
<span data-ttu-id="c4fd2-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4fd2-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fd2-144">CommonParameters</span></span>
<span data-ttu-id="c4fd2-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fd2-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4fd2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fd2-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4fd2-147">INPUTS</span></span>

## <span data-ttu-id="c4fd2-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4fd2-148">OUTPUTS</span></span>

### <span data-ttu-id="c4fd2-149">Dizisi</span><span class="sxs-lookup"><span data-stu-id="c4fd2-149">String</span></span>
<span data-ttu-id="c4fd2-150">Cmdlet, anahtarın yedeğini içeren çıkış dosyasının yolunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="c4fd2-150">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="c4fd2-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4fd2-151">NOTES</span></span>

## <span data-ttu-id="c4fd2-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4fd2-152">RELATED LINKS</span></span>

[<span data-ttu-id="c4fd2-153">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4fd2-153">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="c4fd2-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4fd2-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="c4fd2-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4fd2-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="c4fd2-156">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4fd2-156">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)
