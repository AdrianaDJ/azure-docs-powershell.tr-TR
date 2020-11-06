---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 2a79f4bb555576414b4ed14c06ee0050133e139d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594477"
---
# <span data-ttu-id="12ca4-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="12ca4-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="12ca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="12ca4-103">Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="12ca4-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12ca4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12ca4-104">SYNTAX</span></span>

### <span data-ttu-id="12ca4-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12ca4-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12ca4-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="12ca4-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ca4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="12ca4-107">DESCRIPTION</span></span>
<span data-ttu-id="12ca4-108">Set-AzureKeyVaultCertificateIssuer cmdlet 'i, bir Anahtar Kasası 'nda sertifika vereni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="12ca4-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="12ca4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12ca4-109">EXAMPLES</span></span>

### <span data-ttu-id="12ca4-110">Örnek 1: sertifika vereni ayarlama</span><span class="sxs-lookup"><span data-stu-id="12ca4-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="12ca4-111">Bu komut, sertifika verenin özelliklerini ayarlar ve $Issuer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="12ca4-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="12ca4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12ca4-112">PARAMETERS</span></span>

### <span data-ttu-id="12ca4-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="12ca4-113">-AccountId</span></span>
<span data-ttu-id="12ca4-114">Sertifika verenin hesap KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="12ca4-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-115">-Apıkey</span><span class="sxs-lookup"><span data-stu-id="12ca4-115">-ApiKey</span></span>
<span data-ttu-id="12ca4-116">Sertifika verenin API anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12ca4-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ca4-117">-DefaultProfile</span></span>
<span data-ttu-id="12ca4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="12ca4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12ca4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12ca4-119">-InputObject</span></span>
<span data-ttu-id="12ca4-120">Ayarlanacak sertifika vereni belirtir.</span><span class="sxs-lookup"><span data-stu-id="12ca4-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-121">-Issuerprovider</span><span class="sxs-lookup"><span data-stu-id="12ca4-121">-IssuerProvider</span></span>
<span data-ttu-id="12ca4-122">Sertifika verenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="12ca4-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="12ca4-123">-Name</span></span>
<span data-ttu-id="12ca4-124">Verenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12ca4-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="12ca4-125">-OrganizationDetails</span></span>
<span data-ttu-id="12ca4-126">Verenin birlikte kullanılacak kuruluş ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="12ca4-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="12ca4-127">-PassThru</span></span>
<span data-ttu-id="12ca4-128">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="12ca4-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12ca4-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="12ca4-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="12ca4-130">-VaultName</span></span>
<span data-ttu-id="12ca4-131">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12ca4-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="12ca4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="12ca4-132">-Confirm</span></span>
<span data-ttu-id="12ca4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12ca4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ca4-134">-WhatIf</span></span>
<span data-ttu-id="12ca4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12ca4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12ca4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="12ca4-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ca4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ca4-137">CommonParameters</span></span>
<span data-ttu-id="12ca4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12ca4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ca4-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ca4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ca4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12ca4-140">INPUTS</span></span>

### <span data-ttu-id="12ca4-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="12ca4-141">None</span></span>
<span data-ttu-id="12ca4-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="12ca4-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12ca4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12ca4-143">OUTPUTS</span></span>

### <span data-ttu-id="12ca4-144">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="12ca4-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="12ca4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12ca4-145">NOTES</span></span>

## <span data-ttu-id="12ca4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12ca4-146">RELATED LINKS</span></span>

[<span data-ttu-id="12ca4-147">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="12ca4-147">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="12ca4-148">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="12ca4-148">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

