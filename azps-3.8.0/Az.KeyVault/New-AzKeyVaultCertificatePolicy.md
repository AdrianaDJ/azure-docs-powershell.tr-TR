---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104881"
---
# <span data-ttu-id="5802b-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5802b-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5802b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5802b-102">SYNOPSIS</span></span>
<span data-ttu-id="5802b-103">Bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5802b-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="5802b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5802b-104">SYNTAX</span></span>

### <span data-ttu-id="5802b-105">SubjectName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5802b-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5802b-106">Dnsadları</span><span class="sxs-lookup"><span data-stu-id="5802b-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5802b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5802b-107">DESCRIPTION</span></span>
<span data-ttu-id="5802b-108">**New-Azanahtarvaultcertificatepolicy** cmdlet 'ı, Azure Anahtar Kasası için bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5802b-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="5802b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5802b-109">EXAMPLES</span></span>

### <span data-ttu-id="5802b-110">Örnek 1: sertifika ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5802b-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
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

<span data-ttu-id="5802b-111">Bu komut, altı ay için geçerli olan bir sertifika ilkesi oluşturur ve sertifikayı yenilemek için anahtarı yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="5802b-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="5802b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5802b-112">PARAMETERS</span></span>

### <span data-ttu-id="5802b-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="5802b-113">-CertificateTransparency</span></span>
<span data-ttu-id="5802b-114">Sertifika saydamlığının bu sertifika/veren için etkinleştirilip etkinleştirilmediğini gösterir; belirtilmezse, varsayılan değer ' doğru ' olur</span><span class="sxs-lookup"><span data-stu-id="5802b-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5802b-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="5802b-115">-CertificateType</span></span>
<span data-ttu-id="5802b-116">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="5802b-117">-Eğri</span><span class="sxs-lookup"><span data-stu-id="5802b-117">-Curve</span></span>
<span data-ttu-id="5802b-118">Sertifikanın anahtarının eliptik eğri adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="5802b-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5802b-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5802b-120">P-256</span><span class="sxs-lookup"><span data-stu-id="5802b-120">P-256</span></span>
- <span data-ttu-id="5802b-121">P-384</span><span class="sxs-lookup"><span data-stu-id="5802b-121">P-384</span></span>
- <span data-ttu-id="5802b-122">P-521</span><span class="sxs-lookup"><span data-stu-id="5802b-122">P-521</span></span>
- <span data-ttu-id="5802b-123">P-256K</span><span class="sxs-lookup"><span data-stu-id="5802b-123">P-256K</span></span>
- <span data-ttu-id="5802b-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="5802b-124">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5802b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5802b-125">-DefaultProfile</span></span>
<span data-ttu-id="5802b-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5802b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5802b-127">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="5802b-127">-Disabled</span></span>
<span data-ttu-id="5802b-128">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5802b-128">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="5802b-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="5802b-129">-DnsName</span></span>
<span data-ttu-id="5802b-130">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-130">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="5802b-131">-EKU</span><span class="sxs-lookup"><span data-stu-id="5802b-131">-Ekus</span></span>
<span data-ttu-id="5802b-132">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="5802b-133">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="5802b-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5802b-134">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="5802b-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5802b-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="5802b-136">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="5802b-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="5802b-137">-IssuerName</span></span>
<span data-ttu-id="5802b-138">Sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-138">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="5802b-139">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="5802b-139">-KeyNotExportable</span></span>
<span data-ttu-id="5802b-140">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5802b-140">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="5802b-141">-KeySize</span><span class="sxs-lookup"><span data-stu-id="5802b-141">-KeySize</span></span>
<span data-ttu-id="5802b-142">Sertifikanın anahtar boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="5802b-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5802b-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5802b-144">2048</span><span class="sxs-lookup"><span data-stu-id="5802b-144">2048</span></span>
- <span data-ttu-id="5802b-145">3072</span><span class="sxs-lookup"><span data-stu-id="5802b-145">3072</span></span>
- <span data-ttu-id="5802b-146">4096</span><span class="sxs-lookup"><span data-stu-id="5802b-146">4096</span></span>
- <span data-ttu-id="5802b-147">256</span><span class="sxs-lookup"><span data-stu-id="5802b-147">256</span></span>
- <span data-ttu-id="5802b-148">384</span><span class="sxs-lookup"><span data-stu-id="5802b-148">384</span></span>
- <span data-ttu-id="5802b-149">521</span><span class="sxs-lookup"><span data-stu-id="5802b-149">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5802b-150">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5802b-150">-KeyType</span></span>
<span data-ttu-id="5802b-151">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="5802b-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5802b-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5802b-153">RSA</span><span class="sxs-lookup"><span data-stu-id="5802b-153">RSA</span></span>
- <span data-ttu-id="5802b-154">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="5802b-154">RSA-HSM</span></span>
- <span data-ttu-id="5802b-155">EC SAYıLı</span><span class="sxs-lookup"><span data-stu-id="5802b-155">EC</span></span>
- <span data-ttu-id="5802b-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="5802b-156">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5802b-157">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="5802b-157">-KeyUsage</span></span>
<span data-ttu-id="5802b-158">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-158">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="5802b-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5802b-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5802b-160">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5802b-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5802b-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="5802b-162">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5802b-163">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="5802b-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="5802b-164">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5802b-164">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="5802b-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="5802b-165">-SecretContentType</span></span>
<span data-ttu-id="5802b-166">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="5802b-167">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5802b-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5802b-168">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="5802b-168">application/x-pkcs12</span></span>
- <span data-ttu-id="5802b-169">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="5802b-169">application/x-pem-file</span></span>

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

### <span data-ttu-id="5802b-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="5802b-170">-SubjectName</span></span>
<span data-ttu-id="5802b-171">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-171">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="5802b-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="5802b-172">-ValidityInMonths</span></span>
<span data-ttu-id="5802b-173">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5802b-173">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="5802b-174">-Onay</span><span class="sxs-lookup"><span data-stu-id="5802b-174">-Confirm</span></span>
<span data-ttu-id="5802b-175">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5802b-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5802b-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5802b-176">-WhatIf</span></span>
<span data-ttu-id="5802b-177">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5802b-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5802b-178">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5802b-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5802b-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5802b-179">CommonParameters</span></span>
<span data-ttu-id="5802b-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5802b-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5802b-181">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5802b-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5802b-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5802b-182">INPUTS</span></span>

### <span data-ttu-id="5802b-183">System. String</span><span class="sxs-lookup"><span data-stu-id="5802b-183">System.String</span></span>

### <span data-ttu-id="5802b-184">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="5802b-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5802b-185">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5802b-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5802b-186">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5802b-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5802b-187">System. Koleksiyonlar. Generic. LIST ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="5802b-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="5802b-188">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5802b-188">OUTPUTS</span></span>

### <span data-ttu-id="5802b-189">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5802b-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5802b-190">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5802b-190">NOTES</span></span>

## <span data-ttu-id="5802b-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5802b-191">RELATED LINKS</span></span>

[<span data-ttu-id="5802b-192">Get-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="5802b-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="5802b-193">Set-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="5802b-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

