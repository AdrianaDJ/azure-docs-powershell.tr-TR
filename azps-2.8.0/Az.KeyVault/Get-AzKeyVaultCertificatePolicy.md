---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6635afc19f95f32d7c50ff7a92ba5868a5945e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751677"
---
# <span data-ttu-id="9033c-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9033c-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9033c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9033c-102">SYNOPSIS</span></span>
<span data-ttu-id="9033c-103">Anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="9033c-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="9033c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9033c-104">SYNTAX</span></span>

### <span data-ttu-id="9033c-105">VaultAndCertName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9033c-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9033c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9033c-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9033c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9033c-107">DESCRIPTION</span></span>
<span data-ttu-id="9033c-108">**Get-Azanahtarvaultcertificatepolicy** cmdlet 'ı, Azure Anahtar Kasası 'ndaki anahtar kasasındaki bir sertifikanın ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="9033c-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="9033c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9033c-109">EXAMPLES</span></span>

### <span data-ttu-id="9033c-110">Örnek 1: sertifika ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="9033c-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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

<span data-ttu-id="9033c-111">Bu komut, ContosoKV01 anahtar kasasındaki TestCert01 sertifikasının sertifika ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="9033c-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9033c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9033c-112">PARAMETERS</span></span>

### <span data-ttu-id="9033c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9033c-113">-DefaultProfile</span></span>
<span data-ttu-id="9033c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9033c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9033c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9033c-115">-InputObject</span></span>
<span data-ttu-id="9033c-116">Sertifika nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9033c-116">Certificate Object.</span></span>

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

### <span data-ttu-id="9033c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9033c-117">-Name</span></span>
<span data-ttu-id="9033c-118">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9033c-118">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="9033c-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9033c-119">-VaultName</span></span>
<span data-ttu-id="9033c-120">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9033c-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="9033c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9033c-121">CommonParameters</span></span>
<span data-ttu-id="9033c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9033c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9033c-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9033c-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9033c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9033c-124">INPUTS</span></span>

### <span data-ttu-id="9033c-125">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="9033c-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="9033c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9033c-126">OUTPUTS</span></span>

### <span data-ttu-id="9033c-127">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9033c-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9033c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9033c-128">NOTES</span></span>

## <span data-ttu-id="9033c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9033c-129">RELATED LINKS</span></span>

[<span data-ttu-id="9033c-130">Yeni-Aztuş Vaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="9033c-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9033c-131">Set-Azanahtarvaultcertificatepolicy</span><span class="sxs-lookup"><span data-stu-id="9033c-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

