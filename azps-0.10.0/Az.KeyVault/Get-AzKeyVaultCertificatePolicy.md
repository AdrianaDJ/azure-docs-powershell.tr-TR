---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d525a47dde9551e5d48c7c316cf6844323b75e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935794"
---
# <span data-ttu-id="52da9-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52da9-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="52da9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52da9-102">SYNOPSIS</span></span>
<span data-ttu-id="52da9-103">Anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="52da9-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="52da9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52da9-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52da9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52da9-105">DESCRIPTION</span></span>
<span data-ttu-id="52da9-106">**Get-Azanahtarvaultcertificatepolicy** cmdlet 'ı, Azure Anahtar Kasası 'ndaki anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="52da9-106">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="52da9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52da9-107">EXAMPLES</span></span>

### <span data-ttu-id="52da9-108">Örnek 1: sertifika ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="52da9-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="52da9-109">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının sertifika ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="52da9-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="52da9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52da9-110">PARAMETERS</span></span>

### <span data-ttu-id="52da9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52da9-111">-DefaultProfile</span></span>
<span data-ttu-id="52da9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52da9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52da9-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="52da9-113">-Name</span></span>
<span data-ttu-id="52da9-114">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52da9-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="52da9-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="52da9-115">-VaultName</span></span>
<span data-ttu-id="52da9-116">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52da9-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="52da9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52da9-117">CommonParameters</span></span>
<span data-ttu-id="52da9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52da9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52da9-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52da9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52da9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52da9-120">INPUTS</span></span>

### <span data-ttu-id="52da9-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52da9-121">None</span></span>
<span data-ttu-id="52da9-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="52da9-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52da9-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52da9-123">OUTPUTS</span></span>

### <span data-ttu-id="52da9-124">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52da9-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="52da9-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52da9-125">NOTES</span></span>

## <span data-ttu-id="52da9-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52da9-126">RELATED LINKS</span></span>

[<span data-ttu-id="52da9-127">Yeni-Aztuş Vaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="52da9-127">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="52da9-128">Set-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="52da9-128">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

