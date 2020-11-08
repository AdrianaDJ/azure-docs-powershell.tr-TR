---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267366"
---
# <span data-ttu-id="2778e-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2778e-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2778e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2778e-102">SYNOPSIS</span></span>
<span data-ttu-id="2778e-103">Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2778e-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="2778e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2778e-104">SYNTAX</span></span>

### <span data-ttu-id="2778e-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2778e-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2778e-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="2778e-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2778e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2778e-107">DESCRIPTION</span></span>
<span data-ttu-id="2778e-108">Set-AzKeyVaultCertificateIssuer cmdlet 'i, bir Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2778e-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="2778e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2778e-109">EXAMPLES</span></span>

### <span data-ttu-id="2778e-110">Örnek 1: sertifika vereni ayarlama</span><span class="sxs-lookup"><span data-stu-id="2778e-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="2778e-111">Bu komut, sertifika verenin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2778e-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="2778e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2778e-112">PARAMETERS</span></span>

### <span data-ttu-id="2778e-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="2778e-113">-AccountId</span></span>
<span data-ttu-id="2778e-114">Sertifika verenin hesap KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2778e-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-115">-Apıkey</span><span class="sxs-lookup"><span data-stu-id="2778e-115">-ApiKey</span></span>
<span data-ttu-id="2778e-116">Sertifika verenin API anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2778e-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2778e-117">-DefaultProfile</span></span>
<span data-ttu-id="2778e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2778e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2778e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2778e-119">-InputObject</span></span>
<span data-ttu-id="2778e-120">Ayarlanacak sertifika vereni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2778e-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-121">-Issuerprovider</span><span class="sxs-lookup"><span data-stu-id="2778e-121">-IssuerProvider</span></span>
<span data-ttu-id="2778e-122">Sertifika verenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2778e-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="2778e-123">-Name</span></span>
<span data-ttu-id="2778e-124">Verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2778e-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="2778e-125">-OrganizationDetails</span></span>
<span data-ttu-id="2778e-126">Verenin birlikte kullanılacak kuruluş ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="2778e-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2778e-127">-PassThru</span></span>
<span data-ttu-id="2778e-128">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2778e-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2778e-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2778e-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2778e-130">-VaultName</span></span>
<span data-ttu-id="2778e-131">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2778e-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="2778e-132">-Confirm</span></span>
<span data-ttu-id="2778e-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2778e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2778e-134">-WhatIf</span></span>
<span data-ttu-id="2778e-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2778e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2778e-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2778e-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2778e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2778e-137">CommonParameters</span></span>
<span data-ttu-id="2778e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2778e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2778e-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2778e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2778e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2778e-140">INPUTS</span></span>

### <span data-ttu-id="2778e-141">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="2778e-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="2778e-142">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="2778e-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="2778e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2778e-143">OUTPUTS</span></span>

### <span data-ttu-id="2778e-144">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2778e-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="2778e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2778e-145">NOTES</span></span>

## <span data-ttu-id="2778e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2778e-146">RELATED LINKS</span></span>

[<span data-ttu-id="2778e-147">Get-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="2778e-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="2778e-148">Remove-Azkeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="2778e-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

