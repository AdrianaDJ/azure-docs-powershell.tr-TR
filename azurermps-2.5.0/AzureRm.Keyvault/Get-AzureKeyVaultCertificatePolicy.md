---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 692c639ac42d0a8f2dc2bf121321dfc116ebce1b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939560"
---
# <span data-ttu-id="096ab-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="096ab-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="096ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="096ab-102">SYNOPSIS</span></span>
<span data-ttu-id="096ab-103">Anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="096ab-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="096ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="096ab-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="096ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="096ab-105">DESCRIPTION</span></span>
<span data-ttu-id="096ab-106">**Get-AzureKeyVaultCertificatePolicy** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="096ab-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="096ab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="096ab-107">EXAMPLES</span></span>

### <span data-ttu-id="096ab-108">Örnek 1: sertifika ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="096ab-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="096ab-109">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının sertifika ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="096ab-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="096ab-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="096ab-110">PARAMETERS</span></span>

### <span data-ttu-id="096ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096ab-111">-DefaultProfile</span></span>
<span data-ttu-id="096ab-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="096ab-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="096ab-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="096ab-113">-Name</span></span>
<span data-ttu-id="096ab-114">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="096ab-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="096ab-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="096ab-115">-VaultName</span></span>
<span data-ttu-id="096ab-116">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="096ab-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="096ab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096ab-117">CommonParameters</span></span>
<span data-ttu-id="096ab-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="096ab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096ab-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096ab-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096ab-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="096ab-120">INPUTS</span></span>

## <span data-ttu-id="096ab-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="096ab-121">OUTPUTS</span></span>

### <span data-ttu-id="096ab-122">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="096ab-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="096ab-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="096ab-123">NOTES</span></span>

## <span data-ttu-id="096ab-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="096ab-124">RELATED LINKS</span></span>

[<span data-ttu-id="096ab-125">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="096ab-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="096ab-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="096ab-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

