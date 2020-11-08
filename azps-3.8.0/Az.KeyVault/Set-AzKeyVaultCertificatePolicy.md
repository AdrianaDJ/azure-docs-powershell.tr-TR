---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098020"
---
# <span data-ttu-id="fe8ae-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fe8ae-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fe8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8ae-103">Anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="fe8ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe8ae-104">SYNTAX</span></span>

### <span data-ttu-id="fe8ae-105">ExpandedRenewPercentage (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe8ae-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8ae-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="fe8ae-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe8ae-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="fe8ae-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe8ae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe8ae-108">DESCRIPTION</span></span>
<span data-ttu-id="fe8ae-109">**Set-Azanahtarvaultcertificatepolicy** cmdlet 'i anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="fe8ae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe8ae-110">EXAMPLES</span></span>

### <span data-ttu-id="fe8ae-111">Örnek 1: sertifika ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe8ae-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="fe8ae-112">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="fe8ae-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe8ae-113">PARAMETERS</span></span>

### <span data-ttu-id="fe8ae-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="fe8ae-114">-CertificateTransparency</span></span>
<span data-ttu-id="fe8ae-115">Sertifika saydamlığının bu sertifika/veren için etkinleştirilip etkinleştirilmediğini gösterir; belirtilmezse, varsayılan değer ' doğru ' olur</span><span class="sxs-lookup"><span data-stu-id="fe8ae-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="fe8ae-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="fe8ae-116">-CertificateType</span></span>
<span data-ttu-id="fe8ae-117">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="fe8ae-118">-Eğri</span><span class="sxs-lookup"><span data-stu-id="fe8ae-118">-Curve</span></span>
<span data-ttu-id="fe8ae-119">Sertifikanın anahtarının eliptik eğri adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="fe8ae-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fe8ae-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fe8ae-121">P-256</span><span class="sxs-lookup"><span data-stu-id="fe8ae-121">P-256</span></span>
- <span data-ttu-id="fe8ae-122">P-384</span><span class="sxs-lookup"><span data-stu-id="fe8ae-122">P-384</span></span>
- <span data-ttu-id="fe8ae-123">P-521</span><span class="sxs-lookup"><span data-stu-id="fe8ae-123">P-521</span></span>
- <span data-ttu-id="fe8ae-124">P-256K</span><span class="sxs-lookup"><span data-stu-id="fe8ae-124">P-256K</span></span>
- <span data-ttu-id="fe8ae-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="fe8ae-125">SECP256K1</span></span>

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

### <span data-ttu-id="fe8ae-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8ae-126">-DefaultProfile</span></span>
<span data-ttu-id="fe8ae-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fe8ae-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe8ae-128">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="fe8ae-128">-Disabled</span></span>
<span data-ttu-id="fe8ae-129">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-129">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="fe8ae-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="fe8ae-130">-DnsName</span></span>
<span data-ttu-id="fe8ae-131">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-131">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="fe8ae-132">-EKU</span><span class="sxs-lookup"><span data-stu-id="fe8ae-132">-Ekus</span></span>
<span data-ttu-id="fe8ae-133">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="fe8ae-134">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="fe8ae-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fe8ae-135">Otomatik yenileme başlaması gerektiğinde süre sonundan önceki günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="fe8ae-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fe8ae-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="fe8ae-137">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="fe8ae-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe8ae-138">-InputObject</span></span>
<span data-ttu-id="fe8ae-139">Sertifika ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-139">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="fe8ae-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="fe8ae-140">-IssuerName</span></span>
<span data-ttu-id="fe8ae-141">Bu sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-141">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="fe8ae-142">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="fe8ae-142">-KeyNotExportable</span></span>
<span data-ttu-id="fe8ae-143">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-143">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="fe8ae-144">-KeySize</span><span class="sxs-lookup"><span data-stu-id="fe8ae-144">-KeySize</span></span>
<span data-ttu-id="fe8ae-145">Sertifikanın anahtar boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="fe8ae-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fe8ae-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fe8ae-147">2048</span><span class="sxs-lookup"><span data-stu-id="fe8ae-147">2048</span></span>
- <span data-ttu-id="fe8ae-148">3072</span><span class="sxs-lookup"><span data-stu-id="fe8ae-148">3072</span></span>
- <span data-ttu-id="fe8ae-149">4096</span><span class="sxs-lookup"><span data-stu-id="fe8ae-149">4096</span></span>
- <span data-ttu-id="fe8ae-150">256</span><span class="sxs-lookup"><span data-stu-id="fe8ae-150">256</span></span>
- <span data-ttu-id="fe8ae-151">384</span><span class="sxs-lookup"><span data-stu-id="fe8ae-151">384</span></span>
- <span data-ttu-id="fe8ae-152">521</span><span class="sxs-lookup"><span data-stu-id="fe8ae-152">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe8ae-153">-KeyType</span><span class="sxs-lookup"><span data-stu-id="fe8ae-153">-KeyType</span></span>
<span data-ttu-id="fe8ae-154">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="fe8ae-155">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fe8ae-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fe8ae-156">RSA</span><span class="sxs-lookup"><span data-stu-id="fe8ae-156">RSA</span></span>
- <span data-ttu-id="fe8ae-157">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="fe8ae-157">RSA-HSM</span></span>
- <span data-ttu-id="fe8ae-158">EC SAYıLı</span><span class="sxs-lookup"><span data-stu-id="fe8ae-158">EC</span></span>
- <span data-ttu-id="fe8ae-159">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="fe8ae-159">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8ae-160">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="fe8ae-160">-KeyUsage</span></span>
<span data-ttu-id="fe8ae-161">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-161">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="fe8ae-162">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe8ae-162">-Name</span></span>
<span data-ttu-id="fe8ae-163">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-163">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="fe8ae-164">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fe8ae-164">-PassThru</span></span>
<span data-ttu-id="fe8ae-165">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fe8ae-166">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-166">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe8ae-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fe8ae-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fe8ae-168">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="fe8ae-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fe8ae-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="fe8ae-170">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="fe8ae-171">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="fe8ae-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="fe8ae-172">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-172">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="fe8ae-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="fe8ae-173">-SecretContentType</span></span>
<span data-ttu-id="fe8ae-174">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="fe8ae-175">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fe8ae-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fe8ae-176">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="fe8ae-176">application/x-pkcs12</span></span>
- <span data-ttu-id="fe8ae-177">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="fe8ae-177">application/x-pem-file</span></span>

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

### <span data-ttu-id="fe8ae-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="fe8ae-178">-SubjectName</span></span>
<span data-ttu-id="fe8ae-179">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-179">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="fe8ae-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="fe8ae-180">-ValidityInMonths</span></span>
<span data-ttu-id="fe8ae-181">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-181">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="fe8ae-182">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fe8ae-182">-VaultName</span></span>
<span data-ttu-id="fe8ae-183">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-183">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fe8ae-184">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe8ae-184">-Confirm</span></span>
<span data-ttu-id="fe8ae-185">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe8ae-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe8ae-186">-WhatIf</span></span>
<span data-ttu-id="fe8ae-187">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe8ae-188">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe8ae-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8ae-189">CommonParameters</span></span>
<span data-ttu-id="fe8ae-190">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8ae-191">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fe8ae-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8ae-192">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe8ae-192">INPUTS</span></span>

### <span data-ttu-id="fe8ae-193">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fe8ae-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fe8ae-194">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe8ae-194">OUTPUTS</span></span>

### <span data-ttu-id="fe8ae-195">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fe8ae-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fe8ae-196">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe8ae-196">NOTES</span></span>

## <span data-ttu-id="fe8ae-197">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe8ae-197">RELATED LINKS</span></span>

[<span data-ttu-id="fe8ae-198">Get-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="fe8ae-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="fe8ae-199">Yeni-Aztuş Vaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="fe8ae-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

