---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/import-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 0e41c9be2ebf9951e70dd89b58b838f792eae6e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935791"
---
# <span data-ttu-id="e60b0-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e60b0-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="e60b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e60b0-102">SYNOPSIS</span></span>
<span data-ttu-id="e60b0-103">Bir anahtar kasasına sertifika aktarır.</span><span class="sxs-lookup"><span data-stu-id="e60b0-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="e60b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e60b0-104">SYNTAX</span></span>

### <span data-ttu-id="e60b0-105">Importcertificatefromfile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e60b0-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e60b0-106">Importwithprivatekeyfromfile</span><span class="sxs-lookup"><span data-stu-id="e60b0-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e60b0-107">Importwithprivatekeyfromstring</span><span class="sxs-lookup"><span data-stu-id="e60b0-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e60b0-108">Importwithprivatekeyfromcollection</span><span class="sxs-lookup"><span data-stu-id="e60b0-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e60b0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e60b0-109">DESCRIPTION</span></span>
<span data-ttu-id="e60b0-110">**Import-Azanahtarvaultcertificate** cmdlet 'i bir sertifikayı anahtar kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="e60b0-110">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="e60b0-111">Aşağıdaki yöntemlerden birini kullanarak içeri aktarılacak sertifikayı oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e60b0-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="e60b0-112">Sertifika imzalama isteği oluşturmak ve sertifika yetkilisine göndermek için New-AzKeyVaultCertificateSigningRequest cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e60b0-112">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="e60b0-113">Hem sertifika hem de özel anahtarı içeren. pfx veya. P12 dosyası gibi varolan bir sertifika paketi dosyasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e60b0-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="e60b0-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e60b0-114">EXAMPLES</span></span>

### <span data-ttu-id="e60b0-115">Örnek 1: anahtar kasa sertifikasını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="e60b0-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
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

<span data-ttu-id="e60b0-116">İlk komut ConvertTo-SecureString cmdlet 'ini kullanarak güvenli bir parola oluşturur ve $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e60b0-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="e60b0-117">İkinci komut, ImportCert01 adındaki sertifikayı CosotosoKV01 Key kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="e60b0-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="e60b0-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e60b0-118">PARAMETERS</span></span>

### <span data-ttu-id="e60b0-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="e60b0-119">-CertificateCollection</span></span>
<span data-ttu-id="e60b0-120">Anahtar kasasına eklenecek sertifika koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b0-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60b0-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="e60b0-121">-CertificateString</span></span>
<span data-ttu-id="e60b0-122">Bir sertifika dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b0-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="e60b0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60b0-123">-DefaultProfile</span></span>
<span data-ttu-id="e60b0-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e60b0-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e60b0-125">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="e60b0-125">-FilePath</span></span>
<span data-ttu-id="e60b0-126">Bu cmdlet 'in içeri aktardığından kullanılan sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b0-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60b0-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="e60b0-127">-Name</span></span>
<span data-ttu-id="e60b0-128">Sertifika adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b0-128">Specifies the certificate name.</span></span> <span data-ttu-id="e60b0-129">Bu cmdlet Anahtar Kasası adındaki bir sertifikanın tam etki alanı adını (FQDN), şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e60b0-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="e60b0-130">-Parola</span><span class="sxs-lookup"><span data-stu-id="e60b0-130">-Password</span></span>
<span data-ttu-id="e60b0-131">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b0-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60b0-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e60b0-132">-Tag</span></span>
<span data-ttu-id="e60b0-133">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e60b0-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e60b0-134">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="e60b0-134">For example:</span></span>

<span data-ttu-id="e60b0-135">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e60b0-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e60b0-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e60b0-136">-VaultName</span></span>
<span data-ttu-id="e60b0-137">Bu cmdlet 'in sertifika içeri aktardıkları tuş Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e60b0-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="e60b0-138">Bu cmdlet, bir Anahtar Kasası 'nın tam etki alanı adını (FQDN) ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e60b0-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e60b0-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="e60b0-139">-Confirm</span></span>
<span data-ttu-id="e60b0-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e60b0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e60b0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e60b0-141">-WhatIf</span></span>
<span data-ttu-id="e60b0-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e60b0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e60b0-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e60b0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e60b0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60b0-144">CommonParameters</span></span>
<span data-ttu-id="e60b0-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e60b0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60b0-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e60b0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60b0-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e60b0-147">INPUTS</span></span>

### <span data-ttu-id="e60b0-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e60b0-148">None</span></span>
<span data-ttu-id="e60b0-149">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e60b0-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e60b0-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e60b0-150">OUTPUTS</span></span>

### <span data-ttu-id="e60b0-151">Microsoft. Azure. Commands. Keykasa. modeller. Certificatedemeti</span><span class="sxs-lookup"><span data-stu-id="e60b0-151">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="e60b0-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e60b0-152">NOTES</span></span>

## <span data-ttu-id="e60b0-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e60b0-153">RELATED LINKS</span></span>

[<span data-ttu-id="e60b0-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e60b0-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
