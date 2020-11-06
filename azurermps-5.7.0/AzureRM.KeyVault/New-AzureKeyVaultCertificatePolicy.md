---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: caa0961c1b7aebd5fd2f9883831d733a0fa69f1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593484"
---
# <span data-ttu-id="85918-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="85918-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="85918-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85918-102">SYNOPSIS</span></span>
<span data-ttu-id="85918-103">Bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="85918-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85918-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85918-104">SYNTAX</span></span>

### <span data-ttu-id="85918-105">SubjectName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="85918-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled] [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85918-106">Dnsadları</span><span class="sxs-lookup"><span data-stu-id="85918-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85918-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="85918-107">DESCRIPTION</span></span>
<span data-ttu-id="85918-108">**New-AzureKeyVaultCertificatePolicy** cmdlet 'ı, Azure Anahtar Kasası için bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="85918-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="85918-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85918-109">EXAMPLES</span></span>

### <span data-ttu-id="85918-110">Örnek 1: sertifika ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="85918-110">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="85918-111">Bu komut, altı ay için geçerli olan bir sertifika ilkesi oluşturur ve sertifikayı yenilemek için anahtarı yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="85918-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="85918-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85918-112">PARAMETERS</span></span>

### <span data-ttu-id="85918-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="85918-113">-CertificateType</span></span>
<span data-ttu-id="85918-114">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-114">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85918-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85918-115">-DefaultProfile</span></span>
<span data-ttu-id="85918-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="85918-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85918-117">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="85918-117">-Disabled</span></span>
<span data-ttu-id="85918-118">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="85918-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85918-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="85918-119">-DnsName</span></span>
<span data-ttu-id="85918-120">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="85918-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="85918-121">-Ekus</span></span>
<span data-ttu-id="85918-122">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="85918-123">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="85918-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="85918-124">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="85918-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="85918-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="85918-126">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="85918-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="85918-127">-IssuerName</span></span>
<span data-ttu-id="85918-128">Sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="85918-129">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="85918-129">-KeyNotExportable</span></span>
<span data-ttu-id="85918-130">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85918-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85918-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="85918-131">-KeyType</span></span>
<span data-ttu-id="85918-132">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="85918-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="85918-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85918-134">RSA</span><span class="sxs-lookup"><span data-stu-id="85918-134">RSA</span></span>
- <span data-ttu-id="85918-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="85918-135">RSA-HSM</span></span>

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

### <span data-ttu-id="85918-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="85918-136">-KeyUsage</span></span>
<span data-ttu-id="85918-137">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="85918-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="85918-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="85918-139">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="85918-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="85918-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="85918-141">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="85918-142">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="85918-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="85918-143">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85918-143">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85918-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="85918-144">-SecretContentType</span></span>
<span data-ttu-id="85918-145">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="85918-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="85918-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85918-147">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="85918-147">application/x-pkcs12</span></span>
- <span data-ttu-id="85918-148">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="85918-148">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85918-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="85918-149">-SubjectName</span></span>
<span data-ttu-id="85918-150">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85918-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="85918-151">-ValidityInMonths</span></span>
<span data-ttu-id="85918-152">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85918-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="85918-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="85918-153">-Confirm</span></span>
<span data-ttu-id="85918-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85918-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85918-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85918-155">-WhatIf</span></span>
<span data-ttu-id="85918-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85918-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85918-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="85918-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85918-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85918-158">CommonParameters</span></span>
<span data-ttu-id="85918-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85918-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85918-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85918-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85918-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85918-161">INPUTS</span></span>

### <span data-ttu-id="85918-162">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="85918-162">None</span></span>
<span data-ttu-id="85918-163">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="85918-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85918-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85918-164">OUTPUTS</span></span>

### <span data-ttu-id="85918-165">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="85918-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="85918-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85918-166">NOTES</span></span>

## <span data-ttu-id="85918-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85918-167">RELATED LINKS</span></span>

[<span data-ttu-id="85918-168">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="85918-168">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="85918-169">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="85918-169">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

