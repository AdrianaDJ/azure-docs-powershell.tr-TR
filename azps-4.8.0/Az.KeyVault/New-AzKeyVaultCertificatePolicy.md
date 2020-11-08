---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267208"
---
# <span data-ttu-id="709ad-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="709ad-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="709ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="709ad-102">SYNOPSIS</span></span>
<span data-ttu-id="709ad-103">Bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="709ad-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="709ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="709ad-104">SYNTAX</span></span>

### <span data-ttu-id="709ad-105">SubjectName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="709ad-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="709ad-106">Dnsadları</span><span class="sxs-lookup"><span data-stu-id="709ad-106">DNSNames</span></span>
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

## <span data-ttu-id="709ad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="709ad-107">DESCRIPTION</span></span>
<span data-ttu-id="709ad-108">**New-Azanahtarvaultcertificatepolicy** cmdlet 'ı, Azure Anahtar Kasası için bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="709ad-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="709ad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="709ad-109">EXAMPLES</span></span>

### <span data-ttu-id="709ad-110">Örnek 1: sertifika ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="709ad-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="709ad-111">Bu komut, altı ay için geçerli olan bir sertifika ilkesi oluşturur ve sertifikayı yenilemek için anahtarı yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="709ad-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="709ad-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="709ad-112">Example 2</span></span>

<span data-ttu-id="709ad-113">Bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="709ad-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="709ad-114">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="709ad-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="709ad-115">Örnek 3: konu diğer adı (veya SAN) sertifikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="709ad-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
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

<span data-ttu-id="709ad-116">Bu örnek, 3 DNS adı olan bir SAN sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="709ad-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="709ad-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="709ad-117">PARAMETERS</span></span>

### <span data-ttu-id="709ad-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="709ad-118">-CertificateTransparency</span></span>
<span data-ttu-id="709ad-119">Sertifika saydamlığının bu sertifika/veren için etkinleştirilip etkinleştirilmediğini gösterir; belirtilmezse, varsayılan değer ' doğru ' olur</span><span class="sxs-lookup"><span data-stu-id="709ad-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="709ad-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="709ad-120">-CertificateType</span></span>
<span data-ttu-id="709ad-121">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="709ad-122">-Eğri</span><span class="sxs-lookup"><span data-stu-id="709ad-122">-Curve</span></span>
<span data-ttu-id="709ad-123">Sertifikanın anahtarının eliptik eğri adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="709ad-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="709ad-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="709ad-125">P-256</span><span class="sxs-lookup"><span data-stu-id="709ad-125">P-256</span></span>
- <span data-ttu-id="709ad-126">P-384</span><span class="sxs-lookup"><span data-stu-id="709ad-126">P-384</span></span>
- <span data-ttu-id="709ad-127">P-521</span><span class="sxs-lookup"><span data-stu-id="709ad-127">P-521</span></span>
- <span data-ttu-id="709ad-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="709ad-128">P-256K</span></span>
- <span data-ttu-id="709ad-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="709ad-129">SECP256K1</span></span>

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

### <span data-ttu-id="709ad-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709ad-130">-DefaultProfile</span></span>
<span data-ttu-id="709ad-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="709ad-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="709ad-132">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="709ad-132">-Disabled</span></span>
<span data-ttu-id="709ad-133">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="709ad-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="709ad-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="709ad-134">-DnsName</span></span>
<span data-ttu-id="709ad-135">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="709ad-136">Konu diğer adları (San) DNS adları olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="709ad-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="709ad-137">-EKU</span><span class="sxs-lookup"><span data-stu-id="709ad-137">-Ekus</span></span>
<span data-ttu-id="709ad-138">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="709ad-139">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="709ad-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="709ad-140">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="709ad-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="709ad-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="709ad-142">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="709ad-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="709ad-143">-IssuerName</span></span>
<span data-ttu-id="709ad-144">Sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="709ad-145">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="709ad-145">-KeyNotExportable</span></span>
<span data-ttu-id="709ad-146">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="709ad-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="709ad-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="709ad-147">-KeySize</span></span>
<span data-ttu-id="709ad-148">Sertifikanın anahtar boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="709ad-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="709ad-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="709ad-150">2048</span><span class="sxs-lookup"><span data-stu-id="709ad-150">2048</span></span>
- <span data-ttu-id="709ad-151">3072</span><span class="sxs-lookup"><span data-stu-id="709ad-151">3072</span></span>
- <span data-ttu-id="709ad-152">4096</span><span class="sxs-lookup"><span data-stu-id="709ad-152">4096</span></span>
- <span data-ttu-id="709ad-153">256</span><span class="sxs-lookup"><span data-stu-id="709ad-153">256</span></span>
- <span data-ttu-id="709ad-154">384</span><span class="sxs-lookup"><span data-stu-id="709ad-154">384</span></span>
- <span data-ttu-id="709ad-155">521</span><span class="sxs-lookup"><span data-stu-id="709ad-155">521</span></span>

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

### <span data-ttu-id="709ad-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="709ad-156">-KeyType</span></span>
<span data-ttu-id="709ad-157">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="709ad-158">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="709ad-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="709ad-159">RSA</span><span class="sxs-lookup"><span data-stu-id="709ad-159">RSA</span></span>
- <span data-ttu-id="709ad-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="709ad-160">RSA-HSM</span></span>
- <span data-ttu-id="709ad-161">EC SAYıLı</span><span class="sxs-lookup"><span data-stu-id="709ad-161">EC</span></span>
- <span data-ttu-id="709ad-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="709ad-162">EC-HSM</span></span>

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

### <span data-ttu-id="709ad-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="709ad-163">-KeyUsage</span></span>
<span data-ttu-id="709ad-164">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="709ad-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="709ad-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="709ad-166">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="709ad-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="709ad-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="709ad-168">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="709ad-169">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="709ad-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="709ad-170">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="709ad-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="709ad-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="709ad-171">-SecretContentType</span></span>
<span data-ttu-id="709ad-172">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="709ad-173">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="709ad-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="709ad-174">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="709ad-174">application/x-pkcs12</span></span>
- <span data-ttu-id="709ad-175">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="709ad-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="709ad-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="709ad-176">-SubjectName</span></span>
<span data-ttu-id="709ad-177">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="709ad-178">Parametrede bir özellik içinde virgül (,) veya nokta (.) kullanmanız gerekiyorsa `SubjectName` , özellik alanını tırnak işaretleri içine almalısınız.</span><span class="sxs-lookup"><span data-stu-id="709ad-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="709ad-179">Örneğin, O = "contoso, Ltd." kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="709ad-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="709ad-180">Kuruluş adı alanında.</span><span class="sxs-lookup"><span data-stu-id="709ad-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="709ad-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="709ad-181">-ValidityInMonths</span></span>
<span data-ttu-id="709ad-182">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="709ad-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="709ad-183">-Onay</span><span class="sxs-lookup"><span data-stu-id="709ad-183">-Confirm</span></span>
<span data-ttu-id="709ad-184">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="709ad-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="709ad-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="709ad-185">-WhatIf</span></span>
<span data-ttu-id="709ad-186">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="709ad-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="709ad-187">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="709ad-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="709ad-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709ad-188">CommonParameters</span></span>
<span data-ttu-id="709ad-189">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="709ad-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709ad-190">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="709ad-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709ad-191">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="709ad-191">INPUTS</span></span>

### <span data-ttu-id="709ad-192">System. String</span><span class="sxs-lookup"><span data-stu-id="709ad-192">System.String</span></span>

### <span data-ttu-id="709ad-193">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="709ad-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="709ad-194">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="709ad-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="709ad-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="709ad-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="709ad-196">System. Koleksiyonlar. Generic. LIST ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="709ad-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="709ad-197">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="709ad-197">OUTPUTS</span></span>

### <span data-ttu-id="709ad-198">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="709ad-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="709ad-199">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="709ad-199">NOTES</span></span>

## <span data-ttu-id="709ad-200">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="709ad-200">RELATED LINKS</span></span>

[<span data-ttu-id="709ad-201">Get-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="709ad-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="709ad-202">Set-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="709ad-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

