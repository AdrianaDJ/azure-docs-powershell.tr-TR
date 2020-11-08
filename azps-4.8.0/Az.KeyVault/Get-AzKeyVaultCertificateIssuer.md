---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 1504d4f18c8ab3baee000c2cf8d873df1dd9a177
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267221"
---
# <span data-ttu-id="c792d-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c792d-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c792d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c792d-102">SYNOPSIS</span></span>
<span data-ttu-id="c792d-103">Bir Anahtar Kasası için sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="c792d-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="c792d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c792d-104">SYNTAX</span></span>

### <span data-ttu-id="c792d-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c792d-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c792d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c792d-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c792d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="c792d-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c792d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c792d-108">DESCRIPTION</span></span>
<span data-ttu-id="c792d-109">**Get-Azanahtarvaultcertificateıssuer** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için belirtilen sertifika vereni veya tüm sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="c792d-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c792d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c792d-110">EXAMPLES</span></span>

### <span data-ttu-id="c792d-111">Örnek 1: sertifika vereni alma</span><span class="sxs-lookup"><span data-stu-id="c792d-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="c792d-112">Bu komut, TestIssuer01 adındaki sertifika vereni alır.</span><span class="sxs-lookup"><span data-stu-id="c792d-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="c792d-113">Örnek 2: filtreleme kullanarak sertifika veren sertifikaları listeleyin</span><span class="sxs-lookup"><span data-stu-id="c792d-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="c792d-114">Bu komut, "test" ile başlayan sertifika verenler alır.</span><span class="sxs-lookup"><span data-stu-id="c792d-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="c792d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c792d-115">PARAMETERS</span></span>

### <span data-ttu-id="c792d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c792d-116">-DefaultProfile</span></span>
<span data-ttu-id="c792d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c792d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c792d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c792d-118">-InputObject</span></span>
<span data-ttu-id="c792d-119">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c792d-119">KeyVault object.</span></span>

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

### <span data-ttu-id="c792d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c792d-120">-Name</span></span>
<span data-ttu-id="c792d-121">Alınacak sertifika verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c792d-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="c792d-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c792d-122">-ResourceId</span></span>
<span data-ttu-id="c792d-123">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c792d-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="c792d-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c792d-124">-VaultName</span></span>
<span data-ttu-id="c792d-125">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c792d-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c792d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c792d-126">CommonParameters</span></span>
<span data-ttu-id="c792d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c792d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c792d-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c792d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c792d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c792d-129">INPUTS</span></span>

### <span data-ttu-id="c792d-130">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="c792d-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c792d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c792d-131">System.String</span></span>

## <span data-ttu-id="c792d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c792d-132">OUTPUTS</span></span>

### <span data-ttu-id="c792d-133">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="c792d-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="c792d-134">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="c792d-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c792d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c792d-135">NOTES</span></span>

## <span data-ttu-id="c792d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c792d-136">RELATED LINKS</span></span>

[<span data-ttu-id="c792d-137">Remove-Azkeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="c792d-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="c792d-138">Set-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="c792d-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


