---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultCertificate.md
ms.openlocfilehash: 732d8dc7cfe3c0f8a3bec6eb3157b65bc8437e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590214"
---
# <span data-ttu-id="9b9ea-101">Update-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9b9ea-101">Update-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="9b9ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9b9ea-103">Sertifikanın düzenlenebilir özniteliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b9ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b9ea-104">SYNTAX</span></span>

### <span data-ttu-id="9b9ea-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b9ea-105">ByName (Default)</span></span>
```
Update-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b9ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b9ea-106">ByInputObject</span></span>
```
Update-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b9ea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b9ea-107">DESCRIPTION</span></span>
<span data-ttu-id="9b9ea-108">**Update-AzureKeyVaultCertificate** cmdlet 'i, bir sertifikanın düzenlenebilir özniteliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-108">The **Update-AzureKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="9b9ea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b9ea-109">EXAMPLES</span></span>

### <span data-ttu-id="9b9ea-110">Örnek 1: sertifikayla ilişkili etiketleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="9b9ea-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="9b9ea-111">İlk komut $Tags değişkenine anahtar/değer çiftleri dizisi atar.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="9b9ea-112">İkinci komut, TestCert01 adındaki sertifikanın etiket değerini $Tags olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="9b9ea-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b9ea-113">PARAMETERS</span></span>

### <span data-ttu-id="9b9ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b9ea-114">-DefaultProfile</span></span>
<span data-ttu-id="9b9ea-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b9ea-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="9b9ea-116">-Enable</span></span>
<span data-ttu-id="9b9ea-117">Varsa, değer doğruysa sertifikayı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="9b9ea-118">Değer yanlışsa sertifikayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="9b9ea-119">Belirtilmemişse, sertifikanın etkin/devre dışı durumu değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9ea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b9ea-120">-InputObject</span></span>
<span data-ttu-id="9b9ea-121">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="9b9ea-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9ea-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b9ea-122">-Name</span></span>
<span data-ttu-id="9b9ea-123">Sertifika adı.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-123">Certificate name.</span></span>
<span data-ttu-id="9b9ea-124">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9ea-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9b9ea-125">-PassThru</span></span>
<span data-ttu-id="9b9ea-126">Cmdlet, varsayılan olarak nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="9b9ea-127">Bu anahtar belirtilmişse, sertifika nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-127">If this switch is specified, return certificate object.</span></span>

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

### <span data-ttu-id="9b9ea-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9b9ea-128">-Tag</span></span>
<span data-ttu-id="9b9ea-129">Sertifika etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="9b9ea-130">Belirtilmezse, var olan Etiketler değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="9b9ea-131">Boş bir Hashtable belirterek etiketi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9ea-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9b9ea-132">-VaultName</span></span>
<span data-ttu-id="9b9ea-133">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-133">Vault name.</span></span>
<span data-ttu-id="9b9ea-134">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9b9ea-135">-Version</span><span class="sxs-lookup"><span data-stu-id="9b9ea-135">-Version</span></span>
<span data-ttu-id="9b9ea-136">Sertifika sürümü.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-136">Certificate version.</span></span>
<span data-ttu-id="9b9ea-137">Cmdlet, kasa adından bir sertifikanın FQDN 'sini, şu anda seçili ortamı, sertifika adını ve sertifika sürümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9ea-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b9ea-138">-Confirm</span></span>
<span data-ttu-id="9b9ea-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b9ea-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b9ea-140">-WhatIf</span></span>
<span data-ttu-id="9b9ea-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b9ea-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b9ea-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b9ea-143">CommonParameters</span></span>
<span data-ttu-id="9b9ea-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b9ea-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b9ea-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b9ea-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b9ea-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b9ea-146">INPUTS</span></span>

### <span data-ttu-id="9b9ea-147">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="9b9ea-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="9b9ea-148">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b9ea-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9b9ea-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b9ea-149">OUTPUTS</span></span>

### <span data-ttu-id="9b9ea-150">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9b9ea-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="9b9ea-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b9ea-151">NOTES</span></span>

## <span data-ttu-id="9b9ea-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b9ea-152">RELATED LINKS</span></span>
