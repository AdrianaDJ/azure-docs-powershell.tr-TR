---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939562"
---
# <span data-ttu-id="4109d-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4109d-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4109d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4109d-102">SYNOPSIS</span></span>
<span data-ttu-id="4109d-103">Bir Anahtar Kasası için sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="4109d-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4109d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4109d-104">SYNTAX</span></span>

### <span data-ttu-id="4109d-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4109d-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4109d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4109d-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4109d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4109d-107">DESCRIPTION</span></span>
<span data-ttu-id="4109d-108">**Get-AzureKeyVaultCertificateIssuer** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için belirtilen sertifika vereni veya tüm sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="4109d-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="4109d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4109d-109">EXAMPLES</span></span>

### <span data-ttu-id="4109d-110">Örnek 1: sertifika vereni alma</span><span class="sxs-lookup"><span data-stu-id="4109d-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="4109d-111">Bu komut, TestIssuer01 adındaki sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="4109d-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="4109d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4109d-112">PARAMETERS</span></span>

### <span data-ttu-id="4109d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4109d-113">-DefaultProfile</span></span>
<span data-ttu-id="4109d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4109d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4109d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4109d-115">-Name</span></span>
<span data-ttu-id="4109d-116">Alınacak sertifika verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4109d-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="4109d-117">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4109d-117">-VaultName</span></span>
<span data-ttu-id="4109d-118">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4109d-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4109d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4109d-119">CommonParameters</span></span>
<span data-ttu-id="4109d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4109d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4109d-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4109d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4109d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4109d-122">INPUTS</span></span>

## <span data-ttu-id="4109d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4109d-123">OUTPUTS</span></span>

### <span data-ttu-id="4109d-124">Liste<Microsoft. Azure. Commands. Keykasa. modeller. Certificateıssuerıdentityıtem>, Microsoft</span><span class="sxs-lookup"><span data-stu-id="4109d-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="4109d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4109d-125">NOTES</span></span>

## <span data-ttu-id="4109d-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4109d-126">RELATED LINKS</span></span>

[<span data-ttu-id="4109d-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4109d-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="4109d-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="4109d-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


