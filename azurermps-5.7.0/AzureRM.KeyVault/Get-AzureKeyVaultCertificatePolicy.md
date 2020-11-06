---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 1317b35e957b46e6f39bfb0866e0429c01d35533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588902"
---
# <span data-ttu-id="eafb9-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="eafb9-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="eafb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eafb9-102">SYNOPSIS</span></span>
<span data-ttu-id="eafb9-103">Anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="eafb9-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eafb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eafb9-104">SYNTAX</span></span>

### <span data-ttu-id="eafb9-105">VaultAndCertName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eafb9-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eafb9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="eafb9-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eafb9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eafb9-107">DESCRIPTION</span></span>
<span data-ttu-id="eafb9-108">**Get-AzureKeyVaultCertificatePolicy** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="eafb9-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="eafb9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eafb9-109">EXAMPLES</span></span>

### <span data-ttu-id="eafb9-110">Örnek 1: sertifika ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="eafb9-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="eafb9-111">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının sertifika ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="eafb9-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="eafb9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eafb9-112">PARAMETERS</span></span>

### <span data-ttu-id="eafb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafb9-113">-DefaultProfile</span></span>
<span data-ttu-id="eafb9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eafb9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eafb9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eafb9-115">-InputObject</span></span>
<span data-ttu-id="eafb9-116">Sertifika nesnesi.</span><span class="sxs-lookup"><span data-stu-id="eafb9-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eafb9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="eafb9-117">-Name</span></span>
<span data-ttu-id="eafb9-118">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eafb9-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eafb9-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="eafb9-119">-VaultName</span></span>
<span data-ttu-id="eafb9-120">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eafb9-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eafb9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafb9-121">CommonParameters</span></span>
<span data-ttu-id="eafb9-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eafb9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafb9-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafb9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafb9-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eafb9-124">INPUTS</span></span>

### <span data-ttu-id="eafb9-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eafb9-125">None</span></span>
<span data-ttu-id="eafb9-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="eafb9-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eafb9-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eafb9-127">OUTPUTS</span></span>

### <span data-ttu-id="eafb9-128">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="eafb9-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="eafb9-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eafb9-129">NOTES</span></span>

## <span data-ttu-id="eafb9-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eafb9-130">RELATED LINKS</span></span>

[<span data-ttu-id="eafb9-131">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="eafb9-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="eafb9-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="eafb9-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

