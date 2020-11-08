---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267365"
---
# <span data-ttu-id="ccbcd-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ccbcd-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ccbcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccbcd-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbcd-103">Anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="ccbcd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccbcd-104">SYNTAX</span></span>

### <span data-ttu-id="ccbcd-105">ExpandedRenewPercentage (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ccbcd-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="ccbcd-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="ccbcd-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccbcd-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="ccbcd-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="ccbcd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccbcd-108">DESCRIPTION</span></span>
<span data-ttu-id="ccbcd-109">**Set-Azanahtarvaultcertificatepolicy** cmdlet 'i anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="ccbcd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccbcd-110">EXAMPLES</span></span>

### <span data-ttu-id="ccbcd-111">Örnek 1: sertifika ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="ccbcd-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="ccbcd-112">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="ccbcd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccbcd-113">PARAMETERS</span></span>

### <span data-ttu-id="ccbcd-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="ccbcd-114">-CertificateTransparency</span></span>
<span data-ttu-id="ccbcd-115">Sertifika saydamlığının bu sertifika/veren için etkinleştirilip etkinleştirilmediğini gösterir; belirtilmezse, varsayılan değer ' doğru ' olur.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="ccbcd-116">`-IssuerName` Bu özellik ayarlanırken belirtilmesi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="ccbcd-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="ccbcd-117">-CertificateType</span></span>
<span data-ttu-id="ccbcd-118">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="ccbcd-119">-Eğri</span><span class="sxs-lookup"><span data-stu-id="ccbcd-119">-Curve</span></span>
<span data-ttu-id="ccbcd-120">Sertifikanın anahtarının eliptik eğri adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="ccbcd-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ccbcd-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ccbcd-122">P-256</span><span class="sxs-lookup"><span data-stu-id="ccbcd-122">P-256</span></span>
- <span data-ttu-id="ccbcd-123">P-384</span><span class="sxs-lookup"><span data-stu-id="ccbcd-123">P-384</span></span>
- <span data-ttu-id="ccbcd-124">P-521</span><span class="sxs-lookup"><span data-stu-id="ccbcd-124">P-521</span></span>
- <span data-ttu-id="ccbcd-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="ccbcd-125">P-256K</span></span>
- <span data-ttu-id="ccbcd-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="ccbcd-126">SECP256K1</span></span>

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

### <span data-ttu-id="ccbcd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbcd-127">-DefaultProfile</span></span>
<span data-ttu-id="ccbcd-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ccbcd-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccbcd-129">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="ccbcd-129">-Disabled</span></span>
<span data-ttu-id="ccbcd-130">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="ccbcd-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="ccbcd-131">-DnsName</span></span>
<span data-ttu-id="ccbcd-132">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="ccbcd-133">-EKU</span><span class="sxs-lookup"><span data-stu-id="ccbcd-133">-Ekus</span></span>
<span data-ttu-id="ccbcd-134">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="ccbcd-135">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="ccbcd-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="ccbcd-136">Otomatik yenileme başlaması gerektiğinde süre sonundan önceki günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="ccbcd-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="ccbcd-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="ccbcd-138">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="ccbcd-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccbcd-139">-InputObject</span></span>
<span data-ttu-id="ccbcd-140">Sertifika ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="ccbcd-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="ccbcd-141">-IssuerName</span></span>
<span data-ttu-id="ccbcd-142">Bu sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="ccbcd-143">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="ccbcd-143">-KeyNotExportable</span></span>
<span data-ttu-id="ccbcd-144">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="ccbcd-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="ccbcd-145">-KeySize</span></span>
<span data-ttu-id="ccbcd-146">Sertifikanın anahtar boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="ccbcd-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ccbcd-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ccbcd-148">2048</span><span class="sxs-lookup"><span data-stu-id="ccbcd-148">2048</span></span>
- <span data-ttu-id="ccbcd-149">3072</span><span class="sxs-lookup"><span data-stu-id="ccbcd-149">3072</span></span>
- <span data-ttu-id="ccbcd-150">4096</span><span class="sxs-lookup"><span data-stu-id="ccbcd-150">4096</span></span>
- <span data-ttu-id="ccbcd-151">256</span><span class="sxs-lookup"><span data-stu-id="ccbcd-151">256</span></span>
- <span data-ttu-id="ccbcd-152">384</span><span class="sxs-lookup"><span data-stu-id="ccbcd-152">384</span></span>
- <span data-ttu-id="ccbcd-153">521</span><span class="sxs-lookup"><span data-stu-id="ccbcd-153">521</span></span>

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

### <span data-ttu-id="ccbcd-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ccbcd-154">-KeyType</span></span>
<span data-ttu-id="ccbcd-155">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="ccbcd-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ccbcd-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ccbcd-157">RSA</span><span class="sxs-lookup"><span data-stu-id="ccbcd-157">RSA</span></span>
- <span data-ttu-id="ccbcd-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="ccbcd-158">RSA-HSM</span></span>
- <span data-ttu-id="ccbcd-159">EC SAYıLı</span><span class="sxs-lookup"><span data-stu-id="ccbcd-159">EC</span></span>
- <span data-ttu-id="ccbcd-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="ccbcd-160">EC-HSM</span></span>

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

### <span data-ttu-id="ccbcd-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="ccbcd-161">-KeyUsage</span></span>
<span data-ttu-id="ccbcd-162">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="ccbcd-163">-Ad</span><span class="sxs-lookup"><span data-stu-id="ccbcd-163">-Name</span></span>
<span data-ttu-id="ccbcd-164">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="ccbcd-165">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ccbcd-165">-PassThru</span></span>
<span data-ttu-id="ccbcd-166">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ccbcd-167">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ccbcd-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="ccbcd-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="ccbcd-169">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="ccbcd-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="ccbcd-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="ccbcd-171">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="ccbcd-172">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="ccbcd-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="ccbcd-173">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="ccbcd-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="ccbcd-174">-SecretContentType</span></span>
<span data-ttu-id="ccbcd-175">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="ccbcd-176">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ccbcd-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ccbcd-177">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="ccbcd-177">application/x-pkcs12</span></span>
- <span data-ttu-id="ccbcd-178">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="ccbcd-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="ccbcd-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="ccbcd-179">-SubjectName</span></span>
<span data-ttu-id="ccbcd-180">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="ccbcd-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="ccbcd-181">-ValidityInMonths</span></span>
<span data-ttu-id="ccbcd-182">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="ccbcd-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ccbcd-183">-VaultName</span></span>
<span data-ttu-id="ccbcd-184">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="ccbcd-185">-Onay</span><span class="sxs-lookup"><span data-stu-id="ccbcd-185">-Confirm</span></span>
<span data-ttu-id="ccbcd-186">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbcd-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbcd-187">-WhatIf</span></span>
<span data-ttu-id="ccbcd-188">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccbcd-189">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbcd-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbcd-190">CommonParameters</span></span>
<span data-ttu-id="ccbcd-191">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbcd-192">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ccbcd-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbcd-193">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccbcd-193">INPUTS</span></span>

### <span data-ttu-id="ccbcd-194">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ccbcd-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ccbcd-195">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccbcd-195">OUTPUTS</span></span>

### <span data-ttu-id="ccbcd-196">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ccbcd-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ccbcd-197">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccbcd-197">NOTES</span></span>

## <span data-ttu-id="ccbcd-198">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccbcd-198">RELATED LINKS</span></span>

[<span data-ttu-id="ccbcd-199">Get-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="ccbcd-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="ccbcd-200">Yeni-Aztuş Vaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="ccbcd-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

