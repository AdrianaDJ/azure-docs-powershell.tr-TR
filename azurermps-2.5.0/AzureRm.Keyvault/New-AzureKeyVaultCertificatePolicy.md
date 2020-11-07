---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: b10dd0e034db53af35c930ce1c4588dee2576c75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939146"
---
# <span data-ttu-id="10637-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10637-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="10637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10637-102">SYNOPSIS</span></span>
<span data-ttu-id="10637-103">Bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10637-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10637-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10637-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10637-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10637-105">DESCRIPTION</span></span>
<span data-ttu-id="10637-106">**New-AzureKeyVaultCertificatePolicy** cmdlet 'ı, Azure Anahtar Kasası için bir bellek içi sertifika ilkesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10637-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="10637-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10637-107">EXAMPLES</span></span>

### <span data-ttu-id="10637-108">Örnek 1: sertifika ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="10637-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="10637-109">Bu komut, altı ay için geçerli olan bir sertifika ilkesi oluşturur ve sertifikayı yenilemek için anahtarı yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="10637-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="10637-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10637-110">PARAMETERS</span></span>

### <span data-ttu-id="10637-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="10637-111">-CertificateType</span></span>
<span data-ttu-id="10637-112">Verenin sertifika türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="10637-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10637-113">-DefaultProfile</span></span>
<span data-ttu-id="10637-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="10637-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10637-115">-Devre dışı</span><span class="sxs-lookup"><span data-stu-id="10637-115">-Disabled</span></span>
<span data-ttu-id="10637-116">Sertifika ilkesinin devre dışı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="10637-116">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="10637-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="10637-117">-DnsNames</span></span>
<span data-ttu-id="10637-118">Sertifikadaki DNS adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="10637-119">-EKU</span><span class="sxs-lookup"><span data-stu-id="10637-119">-Ekus</span></span>
<span data-ttu-id="10637-120">Sertifikadaki gelişmiş anahtar kullanımlarının (EKU) kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="10637-121">-Emaılasonu</span><span class="sxs-lookup"><span data-stu-id="10637-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="10637-122">Otomatik bildirim işlemi başlamadan kaç gün önce kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="10637-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="10637-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="10637-124">Bildirim için otomatik işlemin başlaması için gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="10637-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="10637-125">-IssuerName</span></span>
<span data-ttu-id="10637-126">Sertifikanın verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10637-127">-Anahtarda taşınabilir</span><span class="sxs-lookup"><span data-stu-id="10637-127">-KeyNotExportable</span></span>
<span data-ttu-id="10637-128">Anahtarın verilebilir olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10637-128">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="10637-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="10637-129">-KeyType</span></span>
<span data-ttu-id="10637-130">Sertifikayı yedekleyen anahtarın anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="10637-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="10637-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10637-132">RSA</span><span class="sxs-lookup"><span data-stu-id="10637-132">RSA</span></span>
- <span data-ttu-id="10637-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="10637-133">RSA-HSM</span></span>

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

### <span data-ttu-id="10637-134">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="10637-134">-KeyUsage</span></span>
<span data-ttu-id="10637-135">Sertifikadaki Anahtar kullanımları belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="10637-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="10637-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="10637-137">Otomatik olarak sertifika yenileme işleminin başlayacağı günlerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="10637-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="10637-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="10637-139">Sertifika yenileme için otomatik işlemin başlaması gereken yaşam süresinin yüzdesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="10637-140">-Reusekeyuseyenilemesi</span><span class="sxs-lookup"><span data-stu-id="10637-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="10637-141">Sertifikanın yenileme sırasında anahtarı yeniden kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10637-141">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="10637-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="10637-142">-SecretContentType</span></span>
<span data-ttu-id="10637-143">Yeni Anahtar Kasası parolasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="10637-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="10637-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10637-145">uygulama/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="10637-145">application/x-pkcs12</span></span>
- <span data-ttu-id="10637-146">Application/x-PEM-File</span><span class="sxs-lookup"><span data-stu-id="10637-146">application/x-pem-file</span></span>

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

### <span data-ttu-id="10637-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="10637-147">-SubjectName</span></span>
<span data-ttu-id="10637-148">Sertifikanın konu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-148">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="10637-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="10637-149">-ValidityInMonths</span></span>
<span data-ttu-id="10637-150">Sertifikanın geçerli olduğu ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10637-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="10637-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="10637-151">-Confirm</span></span>
<span data-ttu-id="10637-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10637-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10637-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10637-153">-WhatIf</span></span>
<span data-ttu-id="10637-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10637-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10637-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="10637-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10637-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10637-156">CommonParameters</span></span>
<span data-ttu-id="10637-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10637-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10637-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10637-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10637-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10637-159">INPUTS</span></span>

## <span data-ttu-id="10637-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10637-160">OUTPUTS</span></span>

### <span data-ttu-id="10637-161">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10637-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="10637-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10637-162">NOTES</span></span>

## <span data-ttu-id="10637-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10637-163">RELATED LINKS</span></span>

[<span data-ttu-id="10637-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10637-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="10637-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="10637-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

