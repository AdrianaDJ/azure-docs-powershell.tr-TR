---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 5cc7846ae1d5eba5764c524e4edfb470a7cd562b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763842"
---
# <span data-ttu-id="a5d3b-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a5d3b-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="a5d3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d3b-103">Bir anahtar kasasına sertifika aktarır.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5d3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5d3b-104">SYNTAX</span></span>

### <span data-ttu-id="a5d3b-105">Importcertificatefromfile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5d3b-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d3b-106">Importwithprivatekeyfromstring</span><span class="sxs-lookup"><span data-stu-id="a5d3b-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d3b-107">Importwithprivatekeyfromcollection</span><span class="sxs-lookup"><span data-stu-id="a5d3b-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d3b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5d3b-108">DESCRIPTION</span></span>
<span data-ttu-id="a5d3b-109">**Import-AzureKeyVaultCertificate** cmdlet 'i bir sertifikayı anahtar kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="a5d3b-110">Aşağıdaki yöntemlerden birini kullanarak içeri aktarılacak sertifikayı oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a5d3b-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="a5d3b-111">Sertifika imzalama isteği oluşturmak ve sertifika yetkilisine göndermek için New-AzureKeyVaultCertificateSigningRequest cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="a5d3b-112">Hem sertifika hem de özel anahtarı içeren. pfx veya. P12 dosyası gibi varolan bir sertifika paketi dosyasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="a5d3b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5d3b-113">EXAMPLES</span></span>

### <span data-ttu-id="a5d3b-114">Örnek 1: anahtar kasa sertifikasını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="a5d3b-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="a5d3b-115">İlk komut ConvertTo-SecureString cmdlet 'ini kullanarak güvenli bir parola oluşturur ve $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="a5d3b-116">İkinci komut, ImportCert01 adındaki sertifikayı CosotosoKV01 Key kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="a5d3b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5d3b-117">PARAMETERS</span></span>

### <span data-ttu-id="a5d3b-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="a5d3b-118">-CertificateCollection</span></span>
<span data-ttu-id="a5d3b-119">Anahtar kasasına eklenecek sertifika koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d3b-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="a5d3b-120">-CertificateString</span></span>
<span data-ttu-id="a5d3b-121">Bir sertifika dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-121">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d3b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d3b-122">-DefaultProfile</span></span>
<span data-ttu-id="a5d3b-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a5d3b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5d3b-124">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="a5d3b-124">-FilePath</span></span>
<span data-ttu-id="a5d3b-125">Bu cmdlet 'in içeri aktardığından kullanılan sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d3b-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5d3b-126">-Name</span></span>
<span data-ttu-id="a5d3b-127">Sertifika adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-127">Specifies the certificate name.</span></span> <span data-ttu-id="a5d3b-128">Bu cmdlet Anahtar Kasası adındaki bir sertifikanın tam etki alanı adını (FQDN), şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d3b-129">-Parola</span><span class="sxs-lookup"><span data-stu-id="a5d3b-129">-Password</span></span>
<span data-ttu-id="a5d3b-130">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d3b-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a5d3b-131">-Tag</span></span>
<span data-ttu-id="a5d3b-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a5d3b-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="a5d3b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a5d3b-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a5d3b-134">-VaultName</span></span>
<span data-ttu-id="a5d3b-135">Bu cmdlet 'in sertifika içeri aktardıkları tuş Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="a5d3b-136">Bu cmdlet, bir Anahtar Kasası 'nın tam etki alanı adını (FQDN) ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d3b-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5d3b-137">-Confirm</span></span>
<span data-ttu-id="a5d3b-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d3b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d3b-139">-WhatIf</span></span>
<span data-ttu-id="a5d3b-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d3b-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d3b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d3b-142">CommonParameters</span></span>
<span data-ttu-id="a5d3b-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5d3b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d3b-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d3b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d3b-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5d3b-145">INPUTS</span></span>

### <span data-ttu-id="a5d3b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d3b-146">System.String</span></span>

### <span data-ttu-id="a5d3b-147">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="a5d3b-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>
<span data-ttu-id="a5d3b-148">Parametreler: CertificateCollection (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5d3b-148">Parameters: CertificateCollection (ByValue)</span></span>

### <span data-ttu-id="a5d3b-149">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a5d3b-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a5d3b-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5d3b-150">OUTPUTS</span></span>

### <span data-ttu-id="a5d3b-151">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a5d3b-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="a5d3b-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5d3b-152">NOTES</span></span>

## <span data-ttu-id="a5d3b-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5d3b-153">RELATED LINKS</span></span>

[<span data-ttu-id="a5d3b-154">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a5d3b-154">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
