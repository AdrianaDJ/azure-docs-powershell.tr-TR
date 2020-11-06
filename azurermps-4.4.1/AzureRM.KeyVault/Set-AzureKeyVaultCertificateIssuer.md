---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592207"
---
# <span data-ttu-id="94e95-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94e95-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="94e95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94e95-102">SYNOPSIS</span></span>
<span data-ttu-id="94e95-103">Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="94e95-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94e95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94e95-104">SYNTAX</span></span>

### <span data-ttu-id="94e95-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94e95-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e95-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="94e95-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e95-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="94e95-107">DESCRIPTION</span></span>
<span data-ttu-id="94e95-108">Set-AzureKeyVaultCertificateIssuer cmdlet 'i, bir Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="94e95-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="94e95-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94e95-109">EXAMPLES</span></span>

### <span data-ttu-id="94e95-110">Örnek 1: sertifika vereni ayarlama</span><span class="sxs-lookup"><span data-stu-id="94e95-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="94e95-111">Bu komut, sertifika verenin özelliklerini ayarlar ve $Issuer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="94e95-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="94e95-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94e95-112">PARAMETERS</span></span>

### <span data-ttu-id="94e95-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="94e95-113">-AccountId</span></span>
<span data-ttu-id="94e95-114">Sertifika verenin hesap KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="94e95-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e95-115">-Apıkey</span><span class="sxs-lookup"><span data-stu-id="94e95-115">-ApiKey</span></span>
<span data-ttu-id="94e95-116">Sertifika verenin API anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94e95-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e95-117">-Issuer</span><span class="sxs-lookup"><span data-stu-id="94e95-117">-Issuer</span></span>
<span data-ttu-id="94e95-118">Güncelleştirilecek sertifika vereni belirtir.</span><span class="sxs-lookup"><span data-stu-id="94e95-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e95-119">-Issuerprovider</span><span class="sxs-lookup"><span data-stu-id="94e95-119">-IssuerProvider</span></span>
<span data-ttu-id="94e95-120">Sertifika verenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="94e95-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e95-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="94e95-121">-Name</span></span>
<span data-ttu-id="94e95-122">Verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94e95-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e95-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="94e95-123">-OrganizationDetails</span></span>
<span data-ttu-id="94e95-124">Verenin birlikte kullanılacak kuruluş ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="94e95-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94e95-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="94e95-125">-PassThru</span></span>
<span data-ttu-id="94e95-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="94e95-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94e95-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="94e95-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94e95-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="94e95-128">-VaultName</span></span>
<span data-ttu-id="94e95-129">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94e95-129">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="94e95-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="94e95-130">-Confirm</span></span>
<span data-ttu-id="94e95-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94e95-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e95-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e95-132">-WhatIf</span></span>
<span data-ttu-id="94e95-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94e95-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e95-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94e95-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e95-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e95-135">-DefaultProfile</span></span>
<span data-ttu-id="94e95-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94e95-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94e95-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e95-137">CommonParameters</span></span>
<span data-ttu-id="94e95-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94e95-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e95-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e95-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e95-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94e95-140">INPUTS</span></span>

## <span data-ttu-id="94e95-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94e95-141">OUTPUTS</span></span>

### <span data-ttu-id="94e95-142">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="94e95-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="94e95-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94e95-143">NOTES</span></span>

## <span data-ttu-id="94e95-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94e95-144">RELATED LINKS</span></span>

[<span data-ttu-id="94e95-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94e95-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="94e95-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94e95-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

