---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e6ae1be8599869631698ddd886fa09184abfb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751626"
---
# <span data-ttu-id="97f46-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="97f46-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="97f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97f46-102">SYNOPSIS</span></span>
<span data-ttu-id="97f46-103">Anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97f46-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="97f46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97f46-104">SYNTAX</span></span>

### <span data-ttu-id="97f46-105">ExpandedRenewPercentage (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97f46-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97f46-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="97f46-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeySize <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97f46-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="97f46-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97f46-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97f46-108">DESCRIPTION</span></span>
<span data-ttu-id="97f46-109">**Set-Azanahtarvaultcertificatepolicy** cmdlet 'i anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="97f46-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="97f46-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97f46-110">EXAMPLES</span></span>

### <span data-ttu-id="97f46-111">Örnek 1: sertifika ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="97f46-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="97f46-112">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="97f46-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="97f46-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97f46-113">PARAMETERS</span></span>

### <span data-ttu-id="97f46-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="97f46-114">-CertificateTransparency</span></span>
<span data-ttu-id="97f46-115">Sertifika saydamlığının bu sertifika/veren için etkinleştirilip etkinleştirilmediğini gösterir; belirtilmezse, varsayılan değer ' doğru ' olur</span><span class="sxs-lookup"><span data-stu-id="97f46-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="97f46-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="97f46-116">-CertificateType</span></span>
<span data-ttu-id="97f46-117">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="97f46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f46-118">-DefaultProfile</span></span>
<span data-ttu-id="97f46-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="97f46-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97f46-120">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="97f46-120">-Disabled</span></span>
<span data-ttu-id="97f46-121">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="97f46-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="97f46-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="97f46-122">-DnsName</span></span>
<span data-ttu-id="97f46-123">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="97f46-124">-EKU</span><span class="sxs-lookup"><span data-stu-id="97f46-124">-Ekus</span></span>
<span data-ttu-id="97f46-125">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="97f46-126">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="97f46-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="97f46-127">Otomatik yenileme başlaması gerektiğinde süre sonundan önceki günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="97f46-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="97f46-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="97f46-129">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="97f46-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97f46-130">-InputObject</span></span>
<span data-ttu-id="97f46-131">Sertifika ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="97f46-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="97f46-132">-IssuerName</span></span>
<span data-ttu-id="97f46-133">Bu sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="97f46-134">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="97f46-134">-KeyNotExportable</span></span>
<span data-ttu-id="97f46-135">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97f46-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="97f46-136">-KeySize</span><span class="sxs-lookup"><span data-stu-id="97f46-136">-KeySize</span></span>
<span data-ttu-id="97f46-137">Sertifikanın anahtar boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-137">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="97f46-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="97f46-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97f46-139">2048</span><span class="sxs-lookup"><span data-stu-id="97f46-139">2048</span></span>
- <span data-ttu-id="97f46-140">3072</span><span class="sxs-lookup"><span data-stu-id="97f46-140">3072</span></span>
- <span data-ttu-id="97f46-141">4096</span><span class="sxs-lookup"><span data-stu-id="97f46-141">4096</span></span>

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

### <span data-ttu-id="97f46-142">-KeyType</span><span class="sxs-lookup"><span data-stu-id="97f46-142">-KeyType</span></span>
<span data-ttu-id="97f46-143">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-143">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="97f46-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="97f46-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97f46-145">RSA</span><span class="sxs-lookup"><span data-stu-id="97f46-145">RSA</span></span>
- <span data-ttu-id="97f46-146">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="97f46-146">RSA-HSM</span></span>

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

### <span data-ttu-id="97f46-147">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="97f46-147">-KeyUsage</span></span>
<span data-ttu-id="97f46-148">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-148">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="97f46-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="97f46-149">-Name</span></span>
<span data-ttu-id="97f46-150">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-150">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="97f46-151">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="97f46-151">-PassThru</span></span>
<span data-ttu-id="97f46-152">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="97f46-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97f46-153">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="97f46-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97f46-154">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="97f46-154">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="97f46-155">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-155">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="97f46-156">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="97f46-156">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="97f46-157">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-157">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="97f46-158">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="97f46-158">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="97f46-159">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97f46-159">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="97f46-160">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="97f46-160">-SecretContentType</span></span>
<span data-ttu-id="97f46-161">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-161">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="97f46-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="97f46-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97f46-163">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="97f46-163">application/x-pkcs12</span></span>
- <span data-ttu-id="97f46-164">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="97f46-164">application/x-pem-file</span></span>

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

### <span data-ttu-id="97f46-165">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="97f46-165">-SubjectName</span></span>
<span data-ttu-id="97f46-166">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-166">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="97f46-167">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="97f46-167">-ValidityInMonths</span></span>
<span data-ttu-id="97f46-168">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-168">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="97f46-169">-VaultName</span><span class="sxs-lookup"><span data-stu-id="97f46-169">-VaultName</span></span>
<span data-ttu-id="97f46-170">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97f46-170">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="97f46-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="97f46-171">-Confirm</span></span>
<span data-ttu-id="97f46-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97f46-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97f46-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97f46-173">-WhatIf</span></span>
<span data-ttu-id="97f46-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97f46-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97f46-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97f46-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97f46-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f46-176">CommonParameters</span></span>
<span data-ttu-id="97f46-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97f46-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f46-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f46-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f46-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97f46-179">INPUTS</span></span>

### <span data-ttu-id="97f46-180">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="97f46-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="97f46-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97f46-181">OUTPUTS</span></span>

### <span data-ttu-id="97f46-182">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="97f46-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="97f46-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97f46-183">NOTES</span></span>

## <span data-ttu-id="97f46-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97f46-184">RELATED LINKS</span></span>

[<span data-ttu-id="97f46-185">Get-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="97f46-185">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="97f46-186">Yeni-Aztuş Vaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="97f46-186">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

