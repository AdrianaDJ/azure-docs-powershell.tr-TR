---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 271da96d18628c899b10ac17185fd4c3a921d8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588101"
---
# <span data-ttu-id="19299-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="19299-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="19299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19299-102">SYNOPSIS</span></span>
<span data-ttu-id="19299-103">Anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="19299-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19299-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19299-104">SYNTAX</span></span>

### <span data-ttu-id="19299-105">ExpandedRenewPercentage (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19299-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19299-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="19299-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19299-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="19299-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19299-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="19299-108">DESCRIPTION</span></span>
<span data-ttu-id="19299-109">**Set-AzureKeyVaultCertificatePolicy** cmdlet 'i anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="19299-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="19299-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19299-110">EXAMPLES</span></span>

### <span data-ttu-id="19299-111">Örnek 1: sertifika ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="19299-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="19299-112">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19299-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="19299-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19299-113">PARAMETERS</span></span>

### <span data-ttu-id="19299-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="19299-114">-CertificateTransparency</span></span>
<span data-ttu-id="19299-115">Sertifika saydamlığının bu sertifika/veren için etkinleştirilip etkinleştirilmediğini gösterir; belirtilmezse, varsayılan değer ' doğru ' olur</span><span class="sxs-lookup"><span data-stu-id="19299-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="19299-116">-CertificateType</span></span>
<span data-ttu-id="19299-117">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-117">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19299-118">-DefaultProfile</span></span>
<span data-ttu-id="19299-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="19299-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19299-120">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="19299-120">-Disabled</span></span>
<span data-ttu-id="19299-121">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="19299-121">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="19299-122">-DnsName</span></span>
<span data-ttu-id="19299-123">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-123">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-124">-EKU</span><span class="sxs-lookup"><span data-stu-id="19299-124">-Ekus</span></span>
<span data-ttu-id="19299-125">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-126">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="19299-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="19299-127">Otomatik yenileme başlaması gerektiğinde süre sonundan önceki günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="19299-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="19299-129">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19299-130">-InputObject</span></span>
<span data-ttu-id="19299-131">Sertifika ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-131">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19299-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="19299-132">-IssuerName</span></span>
<span data-ttu-id="19299-133">Bu sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-133">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-134">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="19299-134">-KeyNotExportable</span></span>
<span data-ttu-id="19299-135">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19299-135">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-136">-KeyType</span><span class="sxs-lookup"><span data-stu-id="19299-136">-KeyType</span></span>
<span data-ttu-id="19299-137">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-137">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="19299-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19299-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19299-139">RSA</span><span class="sxs-lookup"><span data-stu-id="19299-139">RSA</span></span>
- <span data-ttu-id="19299-140">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="19299-140">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-141">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="19299-141">-KeyUsage</span></span>
<span data-ttu-id="19299-142">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-142">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="19299-143">-Name</span></span>
<span data-ttu-id="19299-144">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-144">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-145">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="19299-145">-PassThru</span></span>
<span data-ttu-id="19299-146">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="19299-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="19299-147">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="19299-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19299-148">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="19299-148">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="19299-149">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-149">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-150">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="19299-150">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="19299-151">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-151">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-152">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="19299-152">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="19299-153">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19299-153">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-154">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="19299-154">-SecretContentType</span></span>
<span data-ttu-id="19299-155">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-155">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="19299-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19299-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19299-157">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="19299-157">application/x-pkcs12</span></span>
- <span data-ttu-id="19299-158">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="19299-158">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-159">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="19299-159">-SubjectName</span></span>
<span data-ttu-id="19299-160">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-160">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-161">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="19299-161">-ValidityInMonths</span></span>
<span data-ttu-id="19299-162">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-162">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-163">-VaultName</span><span class="sxs-lookup"><span data-stu-id="19299-163">-VaultName</span></span>
<span data-ttu-id="19299-164">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19299-164">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19299-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="19299-165">-Confirm</span></span>
<span data-ttu-id="19299-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19299-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19299-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19299-167">-WhatIf</span></span>
<span data-ttu-id="19299-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19299-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19299-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19299-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19299-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19299-170">CommonParameters</span></span>
<span data-ttu-id="19299-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19299-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19299-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19299-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19299-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19299-173">INPUTS</span></span>

### <span data-ttu-id="19299-174">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="19299-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="19299-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19299-175">OUTPUTS</span></span>

### <span data-ttu-id="19299-176">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="19299-176">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="19299-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19299-177">NOTES</span></span>

## <span data-ttu-id="19299-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19299-178">RELATED LINKS</span></span>

[<span data-ttu-id="19299-179">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="19299-179">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="19299-180">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="19299-180">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

