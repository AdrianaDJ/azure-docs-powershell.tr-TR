---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 7a9356952f2ea8b4113f5df0fe364e9647e2c733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939547"
---
# <span data-ttu-id="59f95-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="59f95-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="59f95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f95-102">SYNOPSIS</span></span>
<span data-ttu-id="59f95-103">Anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="59f95-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59f95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59f95-104">SYNTAX</span></span>

### <span data-ttu-id="59f95-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59f95-105">Expanded (Default)</span></span>
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

### <span data-ttu-id="59f95-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="59f95-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f95-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="59f95-107">DESCRIPTION</span></span>
<span data-ttu-id="59f95-108">**Set-AzureKeyVaultCertificatePolicy** cmdlet 'i anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="59f95-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="59f95-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59f95-109">EXAMPLES</span></span>

### <span data-ttu-id="59f95-110">Örnek 1: sertifika ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="59f95-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="59f95-111">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="59f95-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="59f95-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59f95-112">PARAMETERS</span></span>

### <span data-ttu-id="59f95-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="59f95-113">-CertificatePolicy</span></span>
<span data-ttu-id="59f95-114">Sertifika ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-114">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="59f95-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="59f95-115">-CertificateType</span></span>
<span data-ttu-id="59f95-116">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="59f95-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f95-117">-DefaultProfile</span></span>
<span data-ttu-id="59f95-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="59f95-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f95-119">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="59f95-119">-Disabled</span></span>
<span data-ttu-id="59f95-120">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f95-120">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="59f95-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="59f95-121">-DnsNames</span></span>
<span data-ttu-id="59f95-122">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="59f95-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="59f95-123">-Ekus</span></span>
<span data-ttu-id="59f95-124">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="59f95-125">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="59f95-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="59f95-126">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="59f95-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="59f95-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="59f95-128">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="59f95-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="59f95-129">-IssuerName</span></span>
<span data-ttu-id="59f95-130">Bu sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-130">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="59f95-131">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="59f95-131">-KeyNotExportable</span></span>
<span data-ttu-id="59f95-132">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f95-132">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="59f95-133">-KeyType</span><span class="sxs-lookup"><span data-stu-id="59f95-133">-KeyType</span></span>
<span data-ttu-id="59f95-134">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="59f95-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="59f95-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59f95-136">RSA</span><span class="sxs-lookup"><span data-stu-id="59f95-136">RSA</span></span>
- <span data-ttu-id="59f95-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="59f95-137">RSA-HSM</span></span>

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

### <span data-ttu-id="59f95-138">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="59f95-138">-KeyUsage</span></span>
<span data-ttu-id="59f95-139">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="59f95-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="59f95-140">-Name</span></span>
<span data-ttu-id="59f95-141">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="59f95-142">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59f95-142">-PassThru</span></span>
<span data-ttu-id="59f95-143">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="59f95-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59f95-144">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="59f95-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59f95-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="59f95-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="59f95-146">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="59f95-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="59f95-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="59f95-148">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="59f95-149">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="59f95-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="59f95-150">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f95-150">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="59f95-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="59f95-151">-SecretContentType</span></span>
<span data-ttu-id="59f95-152">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="59f95-153">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="59f95-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59f95-154">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="59f95-154">application/x-pkcs12</span></span>
- <span data-ttu-id="59f95-155">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="59f95-155">application/x-pem-file</span></span>

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

### <span data-ttu-id="59f95-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="59f95-156">-SubjectName</span></span>
<span data-ttu-id="59f95-157">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-157">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="59f95-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="59f95-158">-ValidityInMonths</span></span>
<span data-ttu-id="59f95-159">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-159">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="59f95-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="59f95-160">-VaultName</span></span>
<span data-ttu-id="59f95-161">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f95-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="59f95-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="59f95-162">-Confirm</span></span>
<span data-ttu-id="59f95-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59f95-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f95-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f95-164">-WhatIf</span></span>
<span data-ttu-id="59f95-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f95-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f95-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59f95-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f95-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f95-167">CommonParameters</span></span>
<span data-ttu-id="59f95-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59f95-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f95-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f95-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f95-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59f95-170">INPUTS</span></span>

## <span data-ttu-id="59f95-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59f95-171">OUTPUTS</span></span>

### <span data-ttu-id="59f95-172">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="59f95-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="59f95-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59f95-173">NOTES</span></span>

## <span data-ttu-id="59f95-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59f95-174">RELATED LINKS</span></span>

[<span data-ttu-id="59f95-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="59f95-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="59f95-176">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="59f95-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)
