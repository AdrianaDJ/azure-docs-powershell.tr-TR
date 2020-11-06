---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588908"
---
# <span data-ttu-id="de5aa-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de5aa-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="de5aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="de5aa-103">Bir Anahtar Kasası için sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="de5aa-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de5aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de5aa-104">SYNTAX</span></span>

### <span data-ttu-id="de5aa-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="de5aa-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de5aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="de5aa-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de5aa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="de5aa-107">DESCRIPTION</span></span>
<span data-ttu-id="de5aa-108">**Get-AzureKeyVaultCertificateIssuer** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için belirtilen sertifika vereni veya tüm sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="de5aa-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="de5aa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de5aa-109">EXAMPLES</span></span>

### <span data-ttu-id="de5aa-110">Örnek 1: sertifika vereni alma</span><span class="sxs-lookup"><span data-stu-id="de5aa-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="de5aa-111">Bu komut, TestIssuer01 adındaki sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="de5aa-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="de5aa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de5aa-112">PARAMETERS</span></span>

### <span data-ttu-id="de5aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5aa-113">-DefaultProfile</span></span>
<span data-ttu-id="de5aa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="de5aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de5aa-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de5aa-115">-InputObject</span></span>
<span data-ttu-id="de5aa-116">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="de5aa-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de5aa-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="de5aa-117">-Name</span></span>
<span data-ttu-id="de5aa-118">Alınacak sertifika verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5aa-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5aa-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="de5aa-119">-VaultName</span></span>
<span data-ttu-id="de5aa-120">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5aa-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5aa-121">CommonParameters</span></span>
<span data-ttu-id="de5aa-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de5aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5aa-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5aa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5aa-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de5aa-124">INPUTS</span></span>

### <span data-ttu-id="de5aa-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="de5aa-125">None</span></span>
<span data-ttu-id="de5aa-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="de5aa-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de5aa-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de5aa-127">OUTPUTS</span></span>

### <span data-ttu-id="de5aa-128">Liste<Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem>, Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="de5aa-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="de5aa-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de5aa-129">NOTES</span></span>

## <span data-ttu-id="de5aa-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de5aa-130">RELATED LINKS</span></span>

[<span data-ttu-id="de5aa-131">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de5aa-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="de5aa-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="de5aa-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


