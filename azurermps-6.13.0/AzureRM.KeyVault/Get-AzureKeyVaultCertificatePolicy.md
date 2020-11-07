---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 8d03d93a374f2184a995d9cbcdb83050aa98a8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763848"
---
# <span data-ttu-id="017a8-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="017a8-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="017a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="017a8-102">SYNOPSIS</span></span>
<span data-ttu-id="017a8-103">Anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="017a8-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="017a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="017a8-104">SYNTAX</span></span>

### <span data-ttu-id="017a8-105">VaultAndCertName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="017a8-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="017a8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="017a8-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="017a8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="017a8-107">DESCRIPTION</span></span>
<span data-ttu-id="017a8-108">**Get-AzureKeyVaultCertificatePolicy** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="017a8-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="017a8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="017a8-109">EXAMPLES</span></span>

### <span data-ttu-id="017a8-110">Örnek 1: sertifika ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="017a8-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="017a8-111">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının sertifika ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="017a8-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="017a8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="017a8-112">PARAMETERS</span></span>

### <span data-ttu-id="017a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017a8-113">-DefaultProfile</span></span>
<span data-ttu-id="017a8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="017a8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="017a8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="017a8-115">-InputObject</span></span>
<span data-ttu-id="017a8-116">Sertifika nesnesi.</span><span class="sxs-lookup"><span data-stu-id="017a8-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="017a8-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="017a8-117">-Name</span></span>
<span data-ttu-id="017a8-118">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="017a8-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017a8-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="017a8-119">-VaultName</span></span>
<span data-ttu-id="017a8-120">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="017a8-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017a8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017a8-121">CommonParameters</span></span>
<span data-ttu-id="017a8-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="017a8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017a8-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="017a8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017a8-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="017a8-124">INPUTS</span></span>

### <span data-ttu-id="017a8-125">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="017a8-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="017a8-126">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="017a8-126">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="017a8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="017a8-127">OUTPUTS</span></span>

### <span data-ttu-id="017a8-128">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="017a8-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="017a8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="017a8-129">NOTES</span></span>

## <span data-ttu-id="017a8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="017a8-130">RELATED LINKS</span></span>

[<span data-ttu-id="017a8-131">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="017a8-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="017a8-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="017a8-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

