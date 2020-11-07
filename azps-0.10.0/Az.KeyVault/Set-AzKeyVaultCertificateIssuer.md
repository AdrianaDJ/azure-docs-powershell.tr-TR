---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 97faf51b25ee2ae36b028e4a6b992416949a219f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936654"
---
# <span data-ttu-id="1027c-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="1027c-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="1027c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1027c-102">SYNOPSIS</span></span>
<span data-ttu-id="1027c-103">Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1027c-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="1027c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1027c-104">SYNTAX</span></span>

### <span data-ttu-id="1027c-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1027c-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1027c-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="1027c-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1027c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1027c-107">DESCRIPTION</span></span>
<span data-ttu-id="1027c-108">Set-AzKeyVaultCertificateIssuer cmdlet 'i, bir Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1027c-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="1027c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1027c-109">EXAMPLES</span></span>

### <span data-ttu-id="1027c-110">Örnek 1: sertifika vereni ayarlama</span><span class="sxs-lookup"><span data-stu-id="1027c-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="1027c-111">Bu komut, sertifika verenin özelliklerini ayarlar ve $Issuer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1027c-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="1027c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1027c-112">PARAMETERS</span></span>

### <span data-ttu-id="1027c-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="1027c-113">-AccountId</span></span>
<span data-ttu-id="1027c-114">Sertifika verenin hesap KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1027c-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="1027c-115">-Apıkey</span><span class="sxs-lookup"><span data-stu-id="1027c-115">-ApiKey</span></span>
<span data-ttu-id="1027c-116">Sertifika verenin API anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1027c-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1027c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1027c-117">-DefaultProfile</span></span>
<span data-ttu-id="1027c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1027c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1027c-119">-Issuer</span><span class="sxs-lookup"><span data-stu-id="1027c-119">-Issuer</span></span>
<span data-ttu-id="1027c-120">Güncelleştirilecek sertifika vereni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1027c-120">Specifies the certificate issuer to update.</span></span>

```yaml
Type: KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1027c-121">-Issuerprovider</span><span class="sxs-lookup"><span data-stu-id="1027c-121">-IssuerProvider</span></span>
<span data-ttu-id="1027c-122">Sertifika verenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1027c-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="1027c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1027c-123">-Name</span></span>
<span data-ttu-id="1027c-124">Verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1027c-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1027c-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="1027c-125">-OrganizationDetails</span></span>
<span data-ttu-id="1027c-126">Verenin birlikte kullanılacak kuruluş ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="1027c-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1027c-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1027c-127">-PassThru</span></span>
<span data-ttu-id="1027c-128">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1027c-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1027c-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1027c-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1027c-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1027c-130">-VaultName</span></span>
<span data-ttu-id="1027c-131">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1027c-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="1027c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="1027c-132">-Confirm</span></span>
<span data-ttu-id="1027c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1027c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1027c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1027c-134">-WhatIf</span></span>
<span data-ttu-id="1027c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1027c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1027c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1027c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1027c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1027c-137">CommonParameters</span></span>
<span data-ttu-id="1027c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1027c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1027c-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1027c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1027c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1027c-140">INPUTS</span></span>

### <span data-ttu-id="1027c-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1027c-141">None</span></span>
<span data-ttu-id="1027c-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1027c-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1027c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1027c-143">OUTPUTS</span></span>

### <span data-ttu-id="1027c-144">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="1027c-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="1027c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1027c-145">NOTES</span></span>

## <span data-ttu-id="1027c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1027c-146">RELATED LINKS</span></span>

[<span data-ttu-id="1027c-147">Get-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="1027c-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="1027c-148">Remove-Azkeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="1027c-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

