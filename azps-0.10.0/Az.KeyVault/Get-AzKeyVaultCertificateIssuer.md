---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935800"
---
# <span data-ttu-id="100d5-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="100d5-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="100d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="100d5-102">SYNOPSIS</span></span>
<span data-ttu-id="100d5-103">Bir Anahtar Kasası için sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="100d5-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="100d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="100d5-104">SYNTAX</span></span>

### <span data-ttu-id="100d5-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="100d5-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="100d5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="100d5-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="100d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="100d5-107">DESCRIPTION</span></span>
<span data-ttu-id="100d5-108">**Get-Azanahtarvaultcertificateıssuer** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için belirtilen sertifika vereni veya tüm sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="100d5-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="100d5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="100d5-109">EXAMPLES</span></span>

### <span data-ttu-id="100d5-110">Örnek 1: sertifika vereni alma</span><span class="sxs-lookup"><span data-stu-id="100d5-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="100d5-111">Bu komut, TestIssuer01 adındaki sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="100d5-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="100d5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="100d5-112">PARAMETERS</span></span>

### <span data-ttu-id="100d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100d5-113">-DefaultProfile</span></span>
<span data-ttu-id="100d5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="100d5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="100d5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="100d5-115">-Name</span></span>
<span data-ttu-id="100d5-116">Alınacak sertifika verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="100d5-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="100d5-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="100d5-117">-VaultName</span></span>
<span data-ttu-id="100d5-118">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="100d5-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="100d5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100d5-119">CommonParameters</span></span>
<span data-ttu-id="100d5-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="100d5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100d5-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="100d5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100d5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="100d5-122">INPUTS</span></span>

### <span data-ttu-id="100d5-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="100d5-123">None</span></span>
<span data-ttu-id="100d5-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="100d5-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="100d5-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="100d5-125">OUTPUTS</span></span>

### <span data-ttu-id="100d5-126">Liste<Microsoft. Azure. Commands. Keykasa. modeller. Certificateıssuerıdentityıtem>, Microsoft</span><span class="sxs-lookup"><span data-stu-id="100d5-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="100d5-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="100d5-127">NOTES</span></span>

## <span data-ttu-id="100d5-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="100d5-128">RELATED LINKS</span></span>

[<span data-ttu-id="100d5-129">Remove-Azkeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="100d5-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="100d5-130">Set-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="100d5-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


