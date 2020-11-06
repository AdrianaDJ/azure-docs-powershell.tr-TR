---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 94f8b6e136925956faf4402b583d80f6a675cca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594253"
---
# <span data-ttu-id="261a5-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="261a5-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="261a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="261a5-102">SYNOPSIS</span></span>
<span data-ttu-id="261a5-103">Anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="261a5-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="261a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="261a5-104">SYNTAX</span></span>

### <span data-ttu-id="261a5-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="261a5-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="261a5-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="261a5-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="261a5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="261a5-107">DESCRIPTION</span></span>
<span data-ttu-id="261a5-108">**Set-AzureKeyVaultCertificatePolicy** cmdlet 'i anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="261a5-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="261a5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="261a5-109">EXAMPLES</span></span>

### <span data-ttu-id="261a5-110">Örnek 1: sertifika ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="261a5-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="261a5-111">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="261a5-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="261a5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="261a5-112">PARAMETERS</span></span>

### <span data-ttu-id="261a5-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="261a5-113">-CertificatePolicy</span></span>
<span data-ttu-id="261a5-114">Sertifika ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-114">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="261a5-115">-CertificateType</span></span>
<span data-ttu-id="261a5-116">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-117">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="261a5-117">-Disabled</span></span>
<span data-ttu-id="261a5-118">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="261a5-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-119">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="261a5-119">-DnsNames</span></span>
<span data-ttu-id="261a5-120">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="261a5-121">-Ekus</span></span>
<span data-ttu-id="261a5-122">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-123">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="261a5-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="261a5-124">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="261a5-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="261a5-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="261a5-126">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="261a5-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="261a5-127">-IssuerName</span></span>
<span data-ttu-id="261a5-128">Bu sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-128">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-129">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="261a5-129">-KeyNotExportable</span></span>
<span data-ttu-id="261a5-130">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="261a5-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="261a5-131">-KeyType</span></span>
<span data-ttu-id="261a5-132">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="261a5-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="261a5-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="261a5-134">RSA</span><span class="sxs-lookup"><span data-stu-id="261a5-134">RSA</span></span>
- <span data-ttu-id="261a5-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="261a5-135">RSA-HSM</span></span>

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

### <span data-ttu-id="261a5-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="261a5-136">-KeyUsage</span></span>
<span data-ttu-id="261a5-137">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="261a5-138">-Name</span></span>
<span data-ttu-id="261a5-139">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-139">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="261a5-140">-PassThru</span></span>
<span data-ttu-id="261a5-141">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="261a5-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="261a5-142">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="261a5-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="261a5-143">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="261a5-143">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="261a5-144">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-144">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-145">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="261a5-145">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="261a5-146">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-146">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-147">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="261a5-147">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="261a5-148">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="261a5-148">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-149">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="261a5-149">-SecretContentType</span></span>
<span data-ttu-id="261a5-150">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-150">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="261a5-151">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="261a5-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="261a5-152">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="261a5-152">application/x-pkcs12</span></span>
- <span data-ttu-id="261a5-153">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="261a5-153">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-154">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="261a5-154">-SubjectName</span></span>
<span data-ttu-id="261a5-155">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-155">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-156">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="261a5-156">-ValidityInMonths</span></span>
<span data-ttu-id="261a5-157">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-157">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="261a5-158">-VaultName</span></span>
<span data-ttu-id="261a5-159">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="261a5-159">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a5-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="261a5-160">-Confirm</span></span>
<span data-ttu-id="261a5-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="261a5-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="261a5-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="261a5-162">-WhatIf</span></span>
<span data-ttu-id="261a5-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="261a5-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="261a5-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="261a5-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="261a5-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261a5-165">-DefaultProfile</span></span>
<span data-ttu-id="261a5-166">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="261a5-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="261a5-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261a5-167">CommonParameters</span></span>
<span data-ttu-id="261a5-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="261a5-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261a5-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="261a5-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261a5-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="261a5-170">INPUTS</span></span>

## <span data-ttu-id="261a5-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="261a5-171">OUTPUTS</span></span>

### <span data-ttu-id="261a5-172">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="261a5-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="261a5-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="261a5-173">NOTES</span></span>

## <span data-ttu-id="261a5-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="261a5-174">RELATED LINKS</span></span>

[<span data-ttu-id="261a5-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="261a5-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="261a5-176">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="261a5-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

