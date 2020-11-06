---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 381ce302a8404c0bb643db0fc82e392fe53d956a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587906"
---
# <span data-ttu-id="db2b3-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db2b3-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="db2b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="db2b3-103">Bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db2b3-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db2b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db2b3-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db2b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db2b3-105">DESCRIPTION</span></span>
<span data-ttu-id="db2b3-106">**New-AzureKeyVaultCertificatePolicy** cmdlet 'ı, Azure Anahtar Kasası için bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db2b3-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="db2b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db2b3-107">EXAMPLES</span></span>

### <span data-ttu-id="db2b3-108">Örnek 1: sertifika ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="db2b3-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="db2b3-109">Bu komut, altı ay için geçerli olan bir sertifika ilkesi oluşturur ve sertifikayı yenilemek için anahtarı yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="db2b3-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="db2b3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db2b3-110">PARAMETERS</span></span>

### <span data-ttu-id="db2b3-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="db2b3-111">-CertificateType</span></span>
<span data-ttu-id="db2b3-112">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="db2b3-113">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="db2b3-113">-Disabled</span></span>
<span data-ttu-id="db2b3-114">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-114">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="db2b3-115">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="db2b3-115">-DnsNames</span></span>
<span data-ttu-id="db2b3-116">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-116">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="db2b3-117">-EKU</span><span class="sxs-lookup"><span data-stu-id="db2b3-117">-Ekus</span></span>
<span data-ttu-id="db2b3-118">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-118">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="db2b3-119">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="db2b3-119">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="db2b3-120">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-120">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="db2b3-121">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="db2b3-121">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="db2b3-122">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-122">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="db2b3-123">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="db2b3-123">-IssuerName</span></span>
<span data-ttu-id="db2b3-124">Sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-124">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2b3-125">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="db2b3-125">-KeyNotExportable</span></span>
<span data-ttu-id="db2b3-126">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-126">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="db2b3-127">-KeyType</span><span class="sxs-lookup"><span data-stu-id="db2b3-127">-KeyType</span></span>
<span data-ttu-id="db2b3-128">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-128">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="db2b3-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db2b3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db2b3-130">RSA</span><span class="sxs-lookup"><span data-stu-id="db2b3-130">RSA</span></span>
- <span data-ttu-id="db2b3-131">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="db2b3-131">RSA-HSM</span></span>

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

### <span data-ttu-id="db2b3-132">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="db2b3-132">-KeyUsage</span></span>
<span data-ttu-id="db2b3-133">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-133">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="db2b3-134">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="db2b3-134">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="db2b3-135">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-135">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="db2b3-136">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="db2b3-136">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="db2b3-137">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-137">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="db2b3-138">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="db2b3-138">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="db2b3-139">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-139">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="db2b3-140">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="db2b3-140">-SecretContentType</span></span>
<span data-ttu-id="db2b3-141">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-141">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="db2b3-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db2b3-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db2b3-143">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="db2b3-143">application/x-pkcs12</span></span>
- <span data-ttu-id="db2b3-144">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="db2b3-144">application/x-pem-file</span></span>

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

### <span data-ttu-id="db2b3-145">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="db2b3-145">-SubjectName</span></span>
<span data-ttu-id="db2b3-146">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-146">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="db2b3-147">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="db2b3-147">-ValidityInMonths</span></span>
<span data-ttu-id="db2b3-148">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-148">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="db2b3-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="db2b3-149">-Confirm</span></span>
<span data-ttu-id="db2b3-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db2b3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db2b3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2b3-151">-WhatIf</span></span>
<span data-ttu-id="db2b3-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db2b3-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db2b3-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db2b3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db2b3-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2b3-154">-DefaultProfile</span></span>
<span data-ttu-id="db2b3-155">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db2b3-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db2b3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2b3-156">CommonParameters</span></span>
<span data-ttu-id="db2b3-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db2b3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2b3-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2b3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2b3-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db2b3-159">INPUTS</span></span>

## <span data-ttu-id="db2b3-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db2b3-160">OUTPUTS</span></span>

### <span data-ttu-id="db2b3-161">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db2b3-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="db2b3-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db2b3-162">NOTES</span></span>

## <span data-ttu-id="db2b3-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db2b3-163">RELATED LINKS</span></span>

[<span data-ttu-id="db2b3-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db2b3-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="db2b3-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="db2b3-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

