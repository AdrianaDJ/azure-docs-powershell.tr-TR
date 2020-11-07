---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763852"
---
# <span data-ttu-id="a2f37-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a2f37-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a2f37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f37-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f37-103">Bir Anahtar Kasası için sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="a2f37-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2f37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2f37-104">SYNTAX</span></span>

### <span data-ttu-id="a2f37-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a2f37-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2f37-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2f37-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2f37-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a2f37-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2f37-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2f37-108">DESCRIPTION</span></span>
<span data-ttu-id="a2f37-109">**Get-AzureKeyVaultCertificateIssuer** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için belirtilen sertifika vereni veya tüm sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="a2f37-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a2f37-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2f37-110">EXAMPLES</span></span>

### <span data-ttu-id="a2f37-111">Örnek 1: sertifika vereni alma</span><span class="sxs-lookup"><span data-stu-id="a2f37-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="a2f37-112">Bu komut, TestIssuer01 adındaki sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="a2f37-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="a2f37-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2f37-113">PARAMETERS</span></span>

### <span data-ttu-id="a2f37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f37-114">-DefaultProfile</span></span>
<span data-ttu-id="a2f37-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a2f37-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2f37-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2f37-116">-InputObject</span></span>
<span data-ttu-id="a2f37-117">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a2f37-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f37-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2f37-118">-Name</span></span>
<span data-ttu-id="a2f37-119">Alınacak sertifika verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f37-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f37-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a2f37-120">-ResourceId</span></span>
<span data-ttu-id="a2f37-121">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a2f37-121">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f37-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a2f37-122">-VaultName</span></span>
<span data-ttu-id="a2f37-123">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f37-123">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f37-124">CommonParameters</span></span>
<span data-ttu-id="a2f37-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2f37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f37-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2f37-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f37-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2f37-127">INPUTS</span></span>

### <span data-ttu-id="a2f37-128">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="a2f37-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="a2f37-129">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a2f37-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a2f37-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a2f37-130">System.String</span></span>

## <span data-ttu-id="a2f37-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2f37-131">OUTPUTS</span></span>

### <span data-ttu-id="a2f37-132">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="a2f37-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="a2f37-133">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="a2f37-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a2f37-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2f37-134">NOTES</span></span>

## <span data-ttu-id="a2f37-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2f37-135">RELATED LINKS</span></span>

[<span data-ttu-id="a2f37-136">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a2f37-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="a2f37-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a2f37-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


