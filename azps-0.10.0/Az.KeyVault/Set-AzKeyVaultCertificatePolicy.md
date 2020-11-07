---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 160c98b141dbde36786404b58c694772dc86d323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936653"
---
# <span data-ttu-id="2a8c6-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2a8c6-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="2a8c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8c6-103">Anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="2a8c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a8c6-104">SYNTAX</span></span>

### <span data-ttu-id="2a8c6-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2a8c6-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a8c6-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="2a8c6-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a8c6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a8c6-107">DESCRIPTION</span></span>
<span data-ttu-id="2a8c6-108">**Set-Azanahtarvaultcertificatepolicy** cmdlet 'i anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-108">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="2a8c6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a8c6-109">EXAMPLES</span></span>

### <span data-ttu-id="2a8c6-110">Örnek 1: sertifika ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="2a8c6-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="2a8c6-111">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="2a8c6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a8c6-112">PARAMETERS</span></span>

### <span data-ttu-id="2a8c6-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2a8c6-113">-CertificatePolicy</span></span>
<span data-ttu-id="2a8c6-114">Sertifika ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="2a8c6-115">-CertificateType</span></span>
<span data-ttu-id="2a8c6-116">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8c6-117">-DefaultProfile</span></span>
<span data-ttu-id="2a8c6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2a8c6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-119">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="2a8c6-119">-Disabled</span></span>
<span data-ttu-id="2a8c6-120">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="2a8c6-121">-DnsNames</span></span>
<span data-ttu-id="2a8c6-122">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="2a8c6-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="2a8c6-123">-Ekus</span></span>
<span data-ttu-id="2a8c6-124">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="2a8c6-125">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="2a8c6-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="2a8c6-126">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="2a8c6-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="2a8c6-128">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="2a8c6-129">-IssuerName</span></span>
<span data-ttu-id="2a8c6-130">Bu sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-131">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="2a8c6-131">-KeyNotExportable</span></span>
<span data-ttu-id="2a8c6-132">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-133">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2a8c6-133">-KeyType</span></span>
<span data-ttu-id="2a8c6-134">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="2a8c6-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2a8c6-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a8c6-136">RSA</span><span class="sxs-lookup"><span data-stu-id="2a8c6-136">RSA</span></span>
- <span data-ttu-id="2a8c6-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="2a8c6-137">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-138">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="2a8c6-138">-KeyUsage</span></span>
<span data-ttu-id="2a8c6-139">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="2a8c6-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a8c6-140">-Name</span></span>
<span data-ttu-id="2a8c6-141">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-141">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-142">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2a8c6-142">-PassThru</span></span>
<span data-ttu-id="2a8c6-143">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a8c6-144">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="2a8c6-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="2a8c6-146">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="2a8c6-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="2a8c6-148">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-149">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="2a8c6-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="2a8c6-150">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="2a8c6-151">-SecretContentType</span></span>
<span data-ttu-id="2a8c6-152">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="2a8c6-153">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2a8c6-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a8c6-154">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="2a8c6-154">application/x-pkcs12</span></span>
- <span data-ttu-id="2a8c6-155">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="2a8c6-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="2a8c6-156">-SubjectName</span></span>
<span data-ttu-id="2a8c6-157">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="2a8c6-158">-ValidityInMonths</span></span>
<span data-ttu-id="2a8c6-159">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2a8c6-160">-VaultName</span></span>
<span data-ttu-id="2a8c6-161">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-161">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="2a8c6-162">-Confirm</span></span>
<span data-ttu-id="2a8c6-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a8c6-164">-WhatIf</span></span>
<span data-ttu-id="2a8c6-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a8c6-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-166">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c6-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8c6-167">CommonParameters</span></span>
<span data-ttu-id="2a8c6-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8c6-169">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a8c6-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8c6-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a8c6-170">INPUTS</span></span>

### <span data-ttu-id="2a8c6-171">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2a8c6-171">None</span></span>
<span data-ttu-id="2a8c6-172">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2a8c6-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a8c6-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a8c6-173">OUTPUTS</span></span>

### <span data-ttu-id="2a8c6-174">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2a8c6-174">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="2a8c6-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a8c6-175">NOTES</span></span>

## <span data-ttu-id="2a8c6-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a8c6-176">RELATED LINKS</span></span>

[<span data-ttu-id="2a8c6-177">Get-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="2a8c6-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="2a8c6-178">Yeni-Aztuş Vaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="2a8c6-178">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

