---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: fdb90d670034e87c4a08c316b73d4bd15614d872
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751628"
---
# <span data-ttu-id="3e6b6-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="3e6b6-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="3e6b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6b6-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6b6-103">Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="3e6b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e6b6-104">SYNTAX</span></span>

### <span data-ttu-id="3e6b6-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e6b6-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e6b6-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="3e6b6-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e6b6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e6b6-107">DESCRIPTION</span></span>
<span data-ttu-id="3e6b6-108">Set-AzKeyVaultCertificateIssuer cmdlet 'i, bir Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="3e6b6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e6b6-109">EXAMPLES</span></span>

### <span data-ttu-id="3e6b6-110">Örnek 1: sertifika vereni ayarlama</span><span class="sxs-lookup"><span data-stu-id="3e6b6-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="3e6b6-111">Bu komut, sertifika verenin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="3e6b6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e6b6-112">PARAMETERS</span></span>

### <span data-ttu-id="3e6b6-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="3e6b6-113">-AccountId</span></span>
<span data-ttu-id="3e6b6-114">Sertifika verenin hesap KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="3e6b6-115">-Apıkey</span><span class="sxs-lookup"><span data-stu-id="3e6b6-115">-ApiKey</span></span>
<span data-ttu-id="3e6b6-116">Sertifika verenin API anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="3e6b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6b6-117">-DefaultProfile</span></span>
<span data-ttu-id="3e6b6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3e6b6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e6b6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e6b6-119">-InputObject</span></span>
<span data-ttu-id="3e6b6-120">Ayarlanacak sertifika vereni belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="3e6b6-121">-Issuerprovider</span><span class="sxs-lookup"><span data-stu-id="3e6b6-121">-IssuerProvider</span></span>
<span data-ttu-id="3e6b6-122">Sertifika verenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="3e6b6-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e6b6-123">-Name</span></span>
<span data-ttu-id="3e6b6-124">Verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="3e6b6-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="3e6b6-125">-OrganizationDetails</span></span>
<span data-ttu-id="3e6b6-126">Verenin birlikte kullanılacak kuruluş ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="3e6b6-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3e6b6-127">-PassThru</span></span>
<span data-ttu-id="3e6b6-128">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3e6b6-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e6b6-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3e6b6-130">-VaultName</span></span>
<span data-ttu-id="3e6b6-131">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="3e6b6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e6b6-132">-Confirm</span></span>
<span data-ttu-id="3e6b6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e6b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6b6-134">-WhatIf</span></span>
<span data-ttu-id="3e6b6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6b6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e6b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6b6-137">CommonParameters</span></span>
<span data-ttu-id="3e6b6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e6b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6b6-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6b6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6b6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e6b6-140">INPUTS</span></span>

### <span data-ttu-id="3e6b6-141">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="3e6b6-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="3e6b6-142">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıssuerıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="3e6b6-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="3e6b6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e6b6-143">OUTPUTS</span></span>

### <span data-ttu-id="3e6b6-144">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="3e6b6-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="3e6b6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e6b6-145">NOTES</span></span>

## <span data-ttu-id="3e6b6-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e6b6-146">RELATED LINKS</span></span>

[<span data-ttu-id="3e6b6-147">Get-Azanahtarvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="3e6b6-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="3e6b6-148">Remove-Azkeyvaultcertificateıssuer</span><span class="sxs-lookup"><span data-stu-id="3e6b6-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

