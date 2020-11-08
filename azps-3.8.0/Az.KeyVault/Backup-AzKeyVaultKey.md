---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 28f4550ac850b7bcc5bab4c90ec510128a8e2ab0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938237"
---
# <span data-ttu-id="b3ca2-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3ca2-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="b3ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ca2-103">Anahtar kasasındaki bir anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="b3ca2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3ca2-104">SYNTAX</span></span>

### <span data-ttu-id="b3ca2-105">Byanahtaradı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3ca2-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3ca2-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="b3ca2-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3ca2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3ca2-107">DESCRIPTION</span></span>
<span data-ttu-id="b3ca2-108">**Backup-Azanahtarvaultkey** cmdlet 'i, anahtarı indirip bir dosyaya depolayarak bir Anahtar Kasası 'nda belirtilen anahtarı yedekler.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="b3ca2-109">Anahtarın birden çok sürümü varsa, tüm sürümler yedeğe dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="b3ca2-110">İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="b3ca2-111">Yedeklenmiş bir anahtarı, yedeklediğiniz abonelikteki herhangi bir anahtar kasaya geri yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="b3ca2-112">Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b3ca2-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="b3ca2-113">Anahtarınızın bir kopyasını, anahtar kasasındaki anahtarınızı yanlışlıkla silmeniz durumunda çevrimdışı bir kopya olacak şekilde sağlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="b3ca2-114">Anahtar Kasası kullanarak bir anahtar oluşturdunuz ve şimdi anahtarı başka bir Azure bölgesine kopyalamak istiyorsunuz; böylece bu uygulamayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="b3ca2-115">**Yedekleme-Azanahtarvaultkey** cmdlet 'ini kullanarak anahtarı şifreli biçimde alın ve Restore-AzKeyVaultKey cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="b3ca2-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3ca2-116">EXAMPLES</span></span>

### <span data-ttu-id="b3ca2-117">Örnek 1: otomatik olarak oluşturulan bir dosya adıyla anahtarı yedekleme</span><span class="sxs-lookup"><span data-stu-id="b3ca2-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="b3ca2-118">Bu komut Mykeykasası adındaki anahtar kasasından MyKey adlı anahtarı alır ve bu anahtarın bir yedeğini sizin için otomatik olarak adlandırılmış bir dosyaya kaydeder ve dosya adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="b3ca2-119">Örnek 2: anahtarı belirtilen dosya adına yedekleme</span><span class="sxs-lookup"><span data-stu-id="b3ca2-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="b3ca2-120">Bu komut Mykeykasası adındaki anahtar vaultmykey adındaki anahtarı alır ve bu anahtarın yedeğini Backup. blob adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="b3ca2-121">Örnek 3: önceden alınan bir anahtarı belirtilen dosya adına yedekleyin, hedef dosyanın üzerine sormadan dosyaya yazılır.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="b3ca2-122">Bu komut $key adlı anahtarın bir yedeğini oluşturur. $Key adlı kasada ad. VaultName, yedek. blob adlı bir dosyaya, zaten varsa dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="b3ca2-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3ca2-123">PARAMETERS</span></span>

### <span data-ttu-id="b3ca2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ca2-124">-DefaultProfile</span></span>
<span data-ttu-id="b3ca2-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3ca2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3ca2-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b3ca2-126">-Force</span></span>
<span data-ttu-id="b3ca2-127">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="b3ca2-127">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ca2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3ca2-128">-InputObject</span></span>
<span data-ttu-id="b3ca2-129">Yedekleme için anahtar paketi, bir geri alma çağrısının çıkışından alınan ardışık düzen.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ca2-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3ca2-130">-Name</span></span>
<span data-ttu-id="b3ca2-131">Yedekleme için anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ca2-132">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="b3ca2-132">-OutputFile</span></span>
<span data-ttu-id="b3ca2-133">Yedekleme bloonun depolandığı çıkış dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="b3ca2-134">Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir dosya adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="b3ca2-135">Var olan bir çıkış dosyasının adını belirtirseniz, işlem tamamlanmıştır ve yedekleme dosyasının zaten var olduğunu belirten bir hata iletisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ca2-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b3ca2-136">-VaultName</span></span>
<span data-ttu-id="b3ca2-137">Yedekleme anahtarını içeren Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ca2-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3ca2-138">-Confirm</span></span>
<span data-ttu-id="b3ca2-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ca2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ca2-140">-WhatIf</span></span>
<span data-ttu-id="b3ca2-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ca2-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ca2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ca2-143">CommonParameters</span></span>
<span data-ttu-id="b3ca2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ca2-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b3ca2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ca2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3ca2-146">INPUTS</span></span>

### <span data-ttu-id="b3ca2-147">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="b3ca2-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="b3ca2-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3ca2-148">OUTPUTS</span></span>

### <span data-ttu-id="b3ca2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b3ca2-149">System.String</span></span>

## <span data-ttu-id="b3ca2-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3ca2-150">NOTES</span></span>

## <span data-ttu-id="b3ca2-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3ca2-151">RELATED LINKS</span></span>

[<span data-ttu-id="b3ca2-152">Add-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="b3ca2-152">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="b3ca2-153">Get-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="b3ca2-153">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="b3ca2-154">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b3ca2-154">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="b3ca2-155">Restore-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="b3ca2-155">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)
