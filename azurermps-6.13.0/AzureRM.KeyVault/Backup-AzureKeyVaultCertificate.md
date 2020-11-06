---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588110"
---
# <span data-ttu-id="34561-101">Backup-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="34561-101">Backup-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="34561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34561-102">SYNOPSIS</span></span>
<span data-ttu-id="34561-103">Bir Anahtar Kasası içinde bir sertifikayı yedekler.</span><span class="sxs-lookup"><span data-stu-id="34561-103">Backs up a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34561-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34561-104">SYNTAX</span></span>

### <span data-ttu-id="34561-105">ByRef (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34561-105">ByCertificateName (Default)</span></span>
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34561-106">Sertifika</span><span class="sxs-lookup"><span data-stu-id="34561-106">ByCertificate</span></span>
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34561-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="34561-107">DESCRIPTION</span></span>
<span data-ttu-id="34561-108">**Backup-AzureKeyVaultCertificate** cmdlet 'i, belirli bir sertifikayı indirip bir dosyada saklayarak bir anahtar kasasına yedekler.</span><span class="sxs-lookup"><span data-stu-id="34561-108">The **Backup-AzureKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="34561-109">Sertifikada birden çok sürüm varsa, tüm sürümleri yedeğe dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="34561-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="34561-110">İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="34561-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="34561-111">Bir yedeklenen sertifikayı yedeklediğiniz abonelikteki herhangi bir anahtar kasaya geri yükleyebilirsiniz; böylece kasa aynı Azure Coğrafya 'da yer alabilir.</span><span class="sxs-lookup"><span data-stu-id="34561-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="34561-112">Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="34561-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="34561-113">Kasayı yanlışlıkla eski bir şekilde silmeniz durumunda sertifikanın çevrimdışı bir kopyasını tutmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="34561-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="34561-114">Anahtar Kasası kullanarak bir sertifika oluşturdunuz ve şimdi nesneyi başka bir Azure bölgesine kopyalamak istiyor; böylece bu uygulamayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34561-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="34561-115">Sertifikayı şifreli biçimde almak için **Backup-AzureKeyVaultCertificate** cmdlet 'ini kullanın ve ardından **restore-AzureKeyVaultCertificate** cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.</span><span class="sxs-lookup"><span data-stu-id="34561-115">Use the **Backup-AzureKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzureKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="34561-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34561-116">EXAMPLES</span></span>

### <span data-ttu-id="34561-117">Örnek 1: otomatik olarak oluşturulan dosya adıyla sertifikayı yedekleme</span><span class="sxs-lookup"><span data-stu-id="34561-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="34561-118">Bu komut Mykeykasası adındaki anahtar kasasından MyCert adlı sertifikayı alır ve bu sertifikanın yedeğini sizin için otomatik olarak adlandırılan bir dosyaya kaydeder ve dosya adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="34561-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="34561-119">Örnek 2: sertifikayı belirtilen dosya adına yedekleme</span><span class="sxs-lookup"><span data-stu-id="34561-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="34561-120">Bu komut Mykeykasası adındaki anahtar kasasından MyCert adlı sertifikayı alır ve bu sertifikanın yedeğini Backup. blob adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="34561-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="34561-121">Örnek 3: daha önce alınan bir sertifikayı belirtilen dosya adına yedekleyin, hedef dosyanın üzerine sormadan dosyaya yazılır.</span><span class="sxs-lookup"><span data-stu-id="34561-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="34561-122">Bu komut, $cert adlı sertifikanın yedeğini oluşturur. $Cert adlı kasada ad. VaultName, yedek. blob adlı bir dosyaya, zaten varsa dosyanın üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="34561-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="34561-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34561-123">PARAMETERS</span></span>

### <span data-ttu-id="34561-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34561-124">-DefaultProfile</span></span>
<span data-ttu-id="34561-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34561-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34561-126">-Force</span><span class="sxs-lookup"><span data-stu-id="34561-126">-Force</span></span>
<span data-ttu-id="34561-127">Varsa, verilen dosyanın üzerine yaz</span><span class="sxs-lookup"><span data-stu-id="34561-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="34561-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34561-128">-InputObject</span></span>
<span data-ttu-id="34561-129">Yedeklenecek gizli, bir geri alma çağrısının çıkışından alınan ardışık düzen.</span><span class="sxs-lookup"><span data-stu-id="34561-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34561-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="34561-130">-Name</span></span>
<span data-ttu-id="34561-131">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="34561-131">Secret name.</span></span>
<span data-ttu-id="34561-132">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34561-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34561-133">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="34561-133">-OutputFile</span></span>
<span data-ttu-id="34561-134">Çıktı dosyası.</span><span class="sxs-lookup"><span data-stu-id="34561-134">Output file.</span></span>
<span data-ttu-id="34561-135">Sertifikanın yedeğinin depolanacağı çıkış dosyası.</span><span class="sxs-lookup"><span data-stu-id="34561-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="34561-136">Belirtilmezse, varsayılan bir dosya adı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34561-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="34561-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="34561-137">-VaultName</span></span>
<span data-ttu-id="34561-138">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="34561-138">Vault name.</span></span>
<span data-ttu-id="34561-139">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34561-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34561-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="34561-140">-Confirm</span></span>
<span data-ttu-id="34561-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34561-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34561-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34561-142">-WhatIf</span></span>
<span data-ttu-id="34561-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34561-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34561-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34561-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34561-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34561-145">CommonParameters</span></span>
<span data-ttu-id="34561-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34561-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34561-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34561-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34561-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34561-148">INPUTS</span></span>

### <span data-ttu-id="34561-149">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="34561-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="34561-150">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="34561-150">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="34561-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34561-151">OUTPUTS</span></span>

### <span data-ttu-id="34561-152">System. String</span><span class="sxs-lookup"><span data-stu-id="34561-152">System.String</span></span>

## <span data-ttu-id="34561-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34561-153">NOTES</span></span>

## <span data-ttu-id="34561-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34561-154">RELATED LINKS</span></span>
