---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 4d78e325908cf7863177b6bb3e1ebed67f4b36de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096163"
---
# <span data-ttu-id="69089-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="69089-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="69089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69089-102">SYNOPSIS</span></span>
<span data-ttu-id="69089-103">Bir anahtar kasasına sertifika aktarır.</span><span class="sxs-lookup"><span data-stu-id="69089-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="69089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69089-104">SYNTAX</span></span>

### <span data-ttu-id="69089-105">Importcertificatefromfile (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69089-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69089-106">Importwithprivatekeyfromstring</span><span class="sxs-lookup"><span data-stu-id="69089-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69089-107">Importwithprivatekeyfromcollection</span><span class="sxs-lookup"><span data-stu-id="69089-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69089-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="69089-108">DESCRIPTION</span></span>
<span data-ttu-id="69089-109">**Import-Azanahtarvaultcertificate** cmdlet 'i bir sertifikayı anahtar kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="69089-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="69089-110">Aşağıdaki yöntemlerden birini kullanarak içeri aktarılacak sertifikayı oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="69089-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="69089-111">Sertifika imzalama isteği oluşturmak ve sertifika yetkilisine göndermek için New-AzKeyVaultCertificateSigningRequest cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="69089-111">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="69089-112">Hem sertifika hem de özel anahtarı içeren. pfx veya. P12 dosyası gibi varolan bir sertifika paketi dosyasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="69089-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="69089-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69089-113">EXAMPLES</span></span>

### <span data-ttu-id="69089-114">Örnek 1: anahtar kasa sertifikasını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="69089-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

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

<span data-ttu-id="69089-115">İlk komut ConvertTo-SecureString cmdlet 'ini kullanarak güvenli bir parola oluşturur ve $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="69089-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="69089-116">İkinci komut, ImportCert01 adındaki sertifikayı CosotosoKV01 Key kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="69089-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="69089-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69089-117">PARAMETERS</span></span>

### <span data-ttu-id="69089-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="69089-118">-CertificateCollection</span></span>
<span data-ttu-id="69089-119">Anahtar kasasına eklenecek sertifika koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="69089-119">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="69089-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="69089-120">-CertificateString</span></span>
<span data-ttu-id="69089-121">Bir sertifika dizesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="69089-121">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="69089-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69089-122">-DefaultProfile</span></span>
<span data-ttu-id="69089-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="69089-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69089-124">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="69089-124">-FilePath</span></span>
<span data-ttu-id="69089-125">Bu cmdlet 'in içeri aktardığından kullanılan sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="69089-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="69089-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="69089-126">-Name</span></span>
<span data-ttu-id="69089-127">Sertifika adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69089-127">Specifies the certificate name.</span></span> <span data-ttu-id="69089-128">Bu cmdlet Anahtar Kasası adındaki bir sertifikanın tam etki alanı adını (FQDN), şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69089-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="69089-129">-Parola</span><span class="sxs-lookup"><span data-stu-id="69089-129">-Password</span></span>
<span data-ttu-id="69089-130">Sertifika dosyasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69089-130">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="69089-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="69089-131">-Tag</span></span>
<span data-ttu-id="69089-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="69089-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="69089-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="69089-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="69089-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="69089-134">-VaultName</span></span>
<span data-ttu-id="69089-135">Bu cmdlet 'in sertifika içeri aktardıkları tuş Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69089-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="69089-136">Bu cmdlet, bir Anahtar Kasası 'nın tam etki alanı adını (FQDN) ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69089-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="69089-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="69089-137">-Confirm</span></span>
<span data-ttu-id="69089-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69089-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69089-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69089-139">-WhatIf</span></span>
<span data-ttu-id="69089-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69089-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69089-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69089-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69089-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69089-142">CommonParameters</span></span>
<span data-ttu-id="69089-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69089-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69089-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69089-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69089-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69089-145">INPUTS</span></span>

### <span data-ttu-id="69089-146">System. String</span><span class="sxs-lookup"><span data-stu-id="69089-146">System.String</span></span>

### <span data-ttu-id="69089-147">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="69089-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="69089-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="69089-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="69089-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69089-149">OUTPUTS</span></span>

### <span data-ttu-id="69089-150">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="69089-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="69089-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69089-151">NOTES</span></span>

## <span data-ttu-id="69089-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69089-152">RELATED LINKS</span></span>

[<span data-ttu-id="69089-153">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="69089-153">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
