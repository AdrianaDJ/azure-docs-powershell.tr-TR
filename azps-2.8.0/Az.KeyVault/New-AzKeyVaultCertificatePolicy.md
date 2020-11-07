---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 262c539d9ff97983494de0951c9a5d47510b0d28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751663"
---
# <span data-ttu-id="3e80d-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3e80d-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3e80d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e80d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e80d-103">Bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3e80d-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="3e80d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e80d-104">SYNTAX</span></span>

### <span data-ttu-id="3e80d-105">SubjectName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e80d-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e80d-106">Dnsadları</span><span class="sxs-lookup"><span data-stu-id="3e80d-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e80d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e80d-107">DESCRIPTION</span></span>
<span data-ttu-id="3e80d-108">**New-Azanahtarvaultcertificatepolicy** cmdlet 'ı, Azure Anahtar Kasası için bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3e80d-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="3e80d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e80d-109">EXAMPLES</span></span>

### <span data-ttu-id="3e80d-110">Örnek 1: sertifika ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3e80d-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

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

<span data-ttu-id="3e80d-111">Bu komut, altı ay için geçerli olan bir sertifika ilkesi oluşturur ve sertifikayı yenilemek için anahtarı yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="3e80d-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="3e80d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e80d-112">PARAMETERS</span></span>

### <span data-ttu-id="3e80d-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="3e80d-113">-CertificateType</span></span>
<span data-ttu-id="3e80d-114">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e80d-115">-DefaultProfile</span></span>
<span data-ttu-id="3e80d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3e80d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e80d-117">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="3e80d-117">-Disabled</span></span>
<span data-ttu-id="3e80d-118">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="3e80d-119">-DnsName</span></span>
<span data-ttu-id="3e80d-120">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="3e80d-121">-Ekus</span></span>
<span data-ttu-id="3e80d-122">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-123">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="3e80d-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3e80d-124">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3e80d-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="3e80d-126">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="3e80d-127">-IssuerName</span></span>
<span data-ttu-id="3e80d-128">Sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="3e80d-129">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="3e80d-129">-KeyNotExportable</span></span>
<span data-ttu-id="3e80d-130">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-131">-KeySize</span><span class="sxs-lookup"><span data-stu-id="3e80d-131">-KeySize</span></span>
<span data-ttu-id="3e80d-132">Sertifikanın anahtar boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-132">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="3e80d-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3e80d-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e80d-134">2048</span><span class="sxs-lookup"><span data-stu-id="3e80d-134">2048</span></span>
- <span data-ttu-id="3e80d-135">3072</span><span class="sxs-lookup"><span data-stu-id="3e80d-135">3072</span></span>
- <span data-ttu-id="3e80d-136">4096</span><span class="sxs-lookup"><span data-stu-id="3e80d-136">4096</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-137">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3e80d-137">-KeyType</span></span>
<span data-ttu-id="3e80d-138">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-138">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="3e80d-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3e80d-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e80d-140">RSA</span><span class="sxs-lookup"><span data-stu-id="3e80d-140">RSA</span></span>
- <span data-ttu-id="3e80d-141">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="3e80d-141">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-142">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="3e80d-142">-KeyUsage</span></span>
<span data-ttu-id="3e80d-143">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-143">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-144">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="3e80d-144">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="3e80d-145">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-145">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-146">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="3e80d-146">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="3e80d-147">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-147">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-148">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="3e80d-148">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="3e80d-149">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-149">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-150">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="3e80d-150">-SecretContentType</span></span>
<span data-ttu-id="3e80d-151">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-151">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="3e80d-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3e80d-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e80d-153">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="3e80d-153">application/x-pkcs12</span></span>
- <span data-ttu-id="3e80d-154">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="3e80d-154">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-155">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="3e80d-155">-SubjectName</span></span>
<span data-ttu-id="3e80d-156">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-156">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-157">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="3e80d-157">-ValidityInMonths</span></span>
<span data-ttu-id="3e80d-158">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-158">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e80d-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e80d-159">-Confirm</span></span>
<span data-ttu-id="3e80d-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e80d-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e80d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e80d-161">-WhatIf</span></span>
<span data-ttu-id="3e80d-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e80d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e80d-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e80d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e80d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e80d-164">CommonParameters</span></span>
<span data-ttu-id="3e80d-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e80d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e80d-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e80d-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e80d-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e80d-167">INPUTS</span></span>

### <span data-ttu-id="3e80d-168">System. String</span><span class="sxs-lookup"><span data-stu-id="3e80d-168">System.String</span></span>

### <span data-ttu-id="3e80d-169">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="3e80d-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3e80d-170">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="3e80d-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3e80d-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e80d-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3e80d-172">System. Koleksiyonlar. Generic. LIST ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="3e80d-172">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="3e80d-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e80d-173">OUTPUTS</span></span>

### <span data-ttu-id="3e80d-174">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3e80d-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3e80d-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e80d-175">NOTES</span></span>

## <span data-ttu-id="3e80d-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e80d-176">RELATED LINKS</span></span>

[<span data-ttu-id="3e80d-177">Get-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="3e80d-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="3e80d-178">Set-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="3e80d-178">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

