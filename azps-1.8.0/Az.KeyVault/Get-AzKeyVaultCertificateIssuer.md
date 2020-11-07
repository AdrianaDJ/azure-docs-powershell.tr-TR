---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc1ee6f168a417c612e01d02c93d8729cc2563af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916340"
---
# <span data-ttu-id="adeb7-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="adeb7-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="adeb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adeb7-102">SYNOPSIS</span></span>
<span data-ttu-id="adeb7-103">Bir Anahtar Kasası için sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="adeb7-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="adeb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="adeb7-104">SYNTAX</span></span>

### <span data-ttu-id="adeb7-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="adeb7-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adeb7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="adeb7-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adeb7-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="adeb7-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adeb7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="adeb7-108">DESCRIPTION</span></span>
<span data-ttu-id="adeb7-109">**Get-Azanahtarvaultcertificateıssuer** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için belirtilen sertifika vereni veya tüm sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="adeb7-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="adeb7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="adeb7-110">EXAMPLES</span></span>

### <span data-ttu-id="adeb7-111">Örnek 1: sertifika vereni alma</span><span class="sxs-lookup"><span data-stu-id="adeb7-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="adeb7-112">Bu komut, TestIssuer01 adındaki sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="adeb7-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="adeb7-113">Örnek 2: filtreleme kullanarak sertifika veren sertifikaları listeleyin</span><span class="sxs-lookup"><span data-stu-id="adeb7-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="adeb7-114">Bu komut, "test" ile başlayan sertifika verenler alır.</span><span class="sxs-lookup"><span data-stu-id="adeb7-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="adeb7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="adeb7-115">PARAMETERS</span></span>

### <span data-ttu-id="adeb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adeb7-116">-DefaultProfile</span></span>
<span data-ttu-id="adeb7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="adeb7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adeb7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adeb7-118">-InputObject</span></span>
<span data-ttu-id="adeb7-119">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="adeb7-119">KeyVault object.</span></span>

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

### <span data-ttu-id="adeb7-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="adeb7-120">-Name</span></span>
<span data-ttu-id="adeb7-121">Alınacak sertifika verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adeb7-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="adeb7-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="adeb7-122">-ResourceId</span></span>
<span data-ttu-id="adeb7-123">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="adeb7-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="adeb7-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="adeb7-124">-VaultName</span></span>
<span data-ttu-id="adeb7-125">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adeb7-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="adeb7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adeb7-126">CommonParameters</span></span>
<span data-ttu-id="adeb7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="adeb7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adeb7-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="adeb7-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adeb7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="adeb7-129">INPUTS</span></span>

### <span data-ttu-id="adeb7-130">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="adeb7-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="adeb7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="adeb7-131">System.String</span></span>

## <span data-ttu-id="adeb7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="adeb7-132">OUTPUTS</span></span>

### <span data-ttu-id="adeb7-133">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="adeb7-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="adeb7-134">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="adeb7-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="adeb7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="adeb7-135">NOTES</span></span>

## <span data-ttu-id="adeb7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="adeb7-136">RELATED LINKS</span></span>

[<span data-ttu-id="adeb7-137">Remove-Azkeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="adeb7-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="adeb7-138">Set-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="adeb7-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


