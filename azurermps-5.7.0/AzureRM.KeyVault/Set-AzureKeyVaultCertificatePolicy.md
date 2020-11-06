---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594473"
---
# <span data-ttu-id="604c5-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="604c5-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="604c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="604c5-102">SYNOPSIS</span></span>
<span data-ttu-id="604c5-103">Anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="604c5-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="604c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="604c5-104">SYNTAX</span></span>

### <span data-ttu-id="604c5-105">ExpandedRenewPercentage (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="604c5-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="604c5-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="604c5-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="604c5-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="604c5-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="604c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="604c5-108">DESCRIPTION</span></span>
<span data-ttu-id="604c5-109">**Set-AzureKeyVaultCertificatePolicy** cmdlet 'i anahtar kasasındaki bir sertifikanın ilkesini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="604c5-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="604c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="604c5-110">EXAMPLES</span></span>

### <span data-ttu-id="604c5-111">Örnek 1: sertifika ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="604c5-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="604c5-112">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="604c5-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="604c5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="604c5-113">PARAMETERS</span></span>

### <span data-ttu-id="604c5-114">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="604c5-114">-CertificateType</span></span>
<span data-ttu-id="604c5-115">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604c5-116">-DefaultProfile</span></span>
<span data-ttu-id="604c5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="604c5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="604c5-118">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="604c5-118">-Disabled</span></span>
<span data-ttu-id="604c5-119">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="604c5-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="604c5-120">-DnsName</span></span>
<span data-ttu-id="604c5-121">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-122">-EKU</span><span class="sxs-lookup"><span data-stu-id="604c5-122">-Ekus</span></span>
<span data-ttu-id="604c5-123">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-124">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="604c5-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="604c5-125">Otomatik yenileme başlaması gerektiğinde süre sonundan önceki günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="604c5-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="604c5-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="604c5-127">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="604c5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="604c5-128">-InputObject</span></span>
<span data-ttu-id="604c5-129">Sertifika ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="604c5-130">-IssuerName</span></span>
<span data-ttu-id="604c5-131">Bu sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-132">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="604c5-132">-KeyNotExportable</span></span>
<span data-ttu-id="604c5-133">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="604c5-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-134">-KeyType</span><span class="sxs-lookup"><span data-stu-id="604c5-134">-KeyType</span></span>
<span data-ttu-id="604c5-135">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="604c5-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="604c5-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="604c5-137">RSA</span><span class="sxs-lookup"><span data-stu-id="604c5-137">RSA</span></span>
- <span data-ttu-id="604c5-138">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="604c5-138">RSA-HSM</span></span>

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

### <span data-ttu-id="604c5-139">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="604c5-139">-KeyUsage</span></span>
<span data-ttu-id="604c5-140">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="604c5-141">-Name</span></span>
<span data-ttu-id="604c5-142">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="604c5-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="604c5-143">-PassThru</span></span>
<span data-ttu-id="604c5-144">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="604c5-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="604c5-145">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="604c5-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="604c5-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="604c5-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="604c5-147">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="604c5-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="604c5-149">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-150">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="604c5-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="604c5-151">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="604c5-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="604c5-152">-SecretContentType</span></span>
<span data-ttu-id="604c5-153">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="604c5-154">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="604c5-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="604c5-155">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="604c5-155">application/x-pkcs12</span></span>
- <span data-ttu-id="604c5-156">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="604c5-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="604c5-157">-SubjectName</span></span>
<span data-ttu-id="604c5-158">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="604c5-159">-ValidityInMonths</span></span>
<span data-ttu-id="604c5-160">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604c5-161">-VaultName</span><span class="sxs-lookup"><span data-stu-id="604c5-161">-VaultName</span></span>
<span data-ttu-id="604c5-162">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="604c5-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="604c5-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="604c5-163">-Confirm</span></span>
<span data-ttu-id="604c5-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="604c5-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="604c5-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="604c5-165">-WhatIf</span></span>
<span data-ttu-id="604c5-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="604c5-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="604c5-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="604c5-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="604c5-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604c5-168">CommonParameters</span></span>
<span data-ttu-id="604c5-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="604c5-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604c5-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="604c5-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604c5-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="604c5-171">INPUTS</span></span>

### <span data-ttu-id="604c5-172">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="604c5-172">None</span></span>
<span data-ttu-id="604c5-173">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="604c5-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="604c5-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="604c5-174">OUTPUTS</span></span>

### <span data-ttu-id="604c5-175">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="604c5-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="604c5-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="604c5-176">NOTES</span></span>

## <span data-ttu-id="604c5-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="604c5-177">RELATED LINKS</span></span>

[<span data-ttu-id="604c5-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="604c5-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="604c5-179">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="604c5-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

