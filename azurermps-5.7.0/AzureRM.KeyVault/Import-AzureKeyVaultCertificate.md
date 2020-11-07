---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 37befa1434d18241b2f4721523de0ab48bebfd0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764998"
---
# <span data-ttu-id="847b4-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="847b4-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="847b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="847b4-102">SYNOPSIS</span></span>
<span data-ttu-id="847b4-103">Bir anahtar kasasına sertifika aktarır.</span><span class="sxs-lookup"><span data-stu-id="847b4-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="847b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="847b4-104">SYNTAX</span></span>

### <span data-ttu-id="847b4-105">Importcertificatefromfile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="847b4-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="847b4-106">Importwithprivatekeyfromstring</span><span class="sxs-lookup"><span data-stu-id="847b4-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="847b4-107">Importwithprivatekeyfromcollection</span><span class="sxs-lookup"><span data-stu-id="847b4-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="847b4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="847b4-108">DESCRIPTION</span></span>
<span data-ttu-id="847b4-109">**Import-AzureKeyVaultCertificate** cmdlet 'i bir sertifikayı anahtar kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="847b4-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="847b4-110">Aşağıdaki yöntemlerden birini kullanarak içeri aktarılacak sertifikayı oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="847b4-110">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="847b4-111">Sertifika imzalama isteği oluşturmak ve sertifika yetkilisine göndermek için New-AzureKeyVaultCertificateSigningRequest cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="847b4-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="847b4-112">Hem sertifika hem de özel anahtarı içeren. pfx veya. P12 dosyası gibi varolan bir sertifika paketi dosyasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="847b4-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="847b4-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="847b4-113">EXAMPLES</span></span>

### <span data-ttu-id="847b4-114">Örnek 1: anahtar kasa sertifikasını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="847b4-114">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="847b4-115">İlk komut ConvertTo-SecureString cmdlet 'ini kullanarak güvenli bir parola oluşturur ve $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="847b4-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="847b4-116">İkinci komut, ImportCert01 adındaki sertifikayı CosotosoKV01 Key kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="847b4-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="847b4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="847b4-117">PARAMETERS</span></span>

### <span data-ttu-id="847b4-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="847b4-118">-CertificateCollection</span></span>
<span data-ttu-id="847b4-119">Anahtar kasasına eklenecek sertifika koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="847b4-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="847b4-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="847b4-120">-CertificateString</span></span>
<span data-ttu-id="847b4-121">Bir sertifika dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="847b4-121">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847b4-122">-DefaultProfile</span></span>
<span data-ttu-id="847b4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="847b4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="847b4-124">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="847b4-124">-FilePath</span></span>
<span data-ttu-id="847b4-125">Bu cmdlet 'in içeri aktardığından kullanılan sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="847b4-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847b4-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="847b4-126">-Name</span></span>
<span data-ttu-id="847b4-127">Sertifika adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="847b4-127">Specifies the certificate name.</span></span> <span data-ttu-id="847b4-128">Bu cmdlet Anahtar Kasası adındaki bir sertifikanın tam etki alanı adını (FQDN), şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="847b4-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847b4-129">-Parola</span><span class="sxs-lookup"><span data-stu-id="847b4-129">-Password</span></span>
<span data-ttu-id="847b4-130">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="847b4-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847b4-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="847b4-131">-Tag</span></span>
<span data-ttu-id="847b4-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="847b4-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="847b4-133">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="847b4-133">For example:</span></span>

<span data-ttu-id="847b4-134">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="847b4-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847b4-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="847b4-135">-VaultName</span></span>
<span data-ttu-id="847b4-136">Bu cmdlet 'in sertifika içeri aktardıkları tuş Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="847b4-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="847b4-137">Bu cmdlet, bir Anahtar Kasası 'nın tam etki alanı adını (FQDN) ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="847b4-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847b4-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="847b4-138">-Confirm</span></span>
<span data-ttu-id="847b4-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="847b4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="847b4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="847b4-140">-WhatIf</span></span>
<span data-ttu-id="847b4-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="847b4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="847b4-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="847b4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="847b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847b4-143">CommonParameters</span></span>
<span data-ttu-id="847b4-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="847b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847b4-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="847b4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847b4-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="847b4-146">INPUTS</span></span>

### <span data-ttu-id="847b4-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="847b4-147">None</span></span>
<span data-ttu-id="847b4-148">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="847b4-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="847b4-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="847b4-149">OUTPUTS</span></span>

### <span data-ttu-id="847b4-150">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="847b4-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="847b4-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="847b4-151">NOTES</span></span>

## <span data-ttu-id="847b4-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="847b4-152">RELATED LINKS</span></span>

[<span data-ttu-id="847b4-153">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="847b4-153">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
