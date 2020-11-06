---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593561"
---
# <span data-ttu-id="88f20-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="88f20-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="88f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f20-102">SYNOPSIS</span></span>
<span data-ttu-id="88f20-103">Bir Anahtar Kasası için sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="88f20-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88f20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88f20-104">SYNTAX</span></span>

### <span data-ttu-id="88f20-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88f20-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88f20-106">ByName</span><span class="sxs-lookup"><span data-stu-id="88f20-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88f20-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="88f20-107">DESCRIPTION</span></span>
<span data-ttu-id="88f20-108">**Get-AzureKeyVaultCertificateIssuer** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için belirtilen sertifika vereni veya tüm sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="88f20-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="88f20-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88f20-109">EXAMPLES</span></span>

### <span data-ttu-id="88f20-110">Örnek 1: sertifika vereni alma</span><span class="sxs-lookup"><span data-stu-id="88f20-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="88f20-111">Bu komut, TestIssuer01 adındaki sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="88f20-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="88f20-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88f20-112">PARAMETERS</span></span>

### <span data-ttu-id="88f20-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="88f20-113">-Name</span></span>
<span data-ttu-id="88f20-114">Alınacak sertifika verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88f20-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f20-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="88f20-115">-VaultName</span></span>
<span data-ttu-id="88f20-116">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88f20-116">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f20-117">-DefaultProfile</span></span>
<span data-ttu-id="88f20-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88f20-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88f20-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f20-119">CommonParameters</span></span>
<span data-ttu-id="88f20-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88f20-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f20-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88f20-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f20-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88f20-122">INPUTS</span></span>

## <span data-ttu-id="88f20-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88f20-123">OUTPUTS</span></span>

### <span data-ttu-id="88f20-124">Liste<Microsoft. Azure. Commands. Keykasa. modeller. Certificateıssuerıdentityıtem>, Microsoft</span><span class="sxs-lookup"><span data-stu-id="88f20-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="88f20-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88f20-125">NOTES</span></span>

## <span data-ttu-id="88f20-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88f20-126">RELATED LINKS</span></span>

[<span data-ttu-id="88f20-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="88f20-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="88f20-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="88f20-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


