---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
ms.openlocfilehash: 8c4bb4813c2d07577d80743906a4f8155bc81282
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937731"
---
# <span data-ttu-id="2a04d-101">Update-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2a04d-101">Update-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="2a04d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a04d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a04d-103">Sertifikanın düzenlenebilir özniteliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2a04d-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="2a04d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a04d-104">SYNTAX</span></span>

### <span data-ttu-id="2a04d-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2a04d-105">ByName (Default)</span></span>
```
Update-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a04d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a04d-106">ByInputObject</span></span>
```
Update-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a04d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a04d-107">DESCRIPTION</span></span>
<span data-ttu-id="2a04d-108">**Update-Azanahtarvaultcertificate** cmdlet 'i, bir sertifikanın düzenlenebilir özniteliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2a04d-108">The **Update-AzKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="2a04d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a04d-109">EXAMPLES</span></span>

### <span data-ttu-id="2a04d-110">Örnek 1: sertifikayla ilişkili etiketleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="2a04d-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

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

<span data-ttu-id="2a04d-111">İlk komut $Tags değişkenine anahtar/değer çiftleri dizisi atar.</span><span class="sxs-lookup"><span data-stu-id="2a04d-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="2a04d-112">İkinci komut, TestCert01 adındaki sertifikanın etiket değerini $Tags olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2a04d-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="2a04d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a04d-113">PARAMETERS</span></span>

### <span data-ttu-id="2a04d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a04d-114">-DefaultProfile</span></span>
<span data-ttu-id="2a04d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a04d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a04d-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="2a04d-116">-Enable</span></span>
<span data-ttu-id="2a04d-117">Varsa, değer doğruysa sertifikayı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="2a04d-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="2a04d-118">Değer yanlışsa sertifikayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="2a04d-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="2a04d-119">Belirtilmemişse, sertifikanın etkin/devre dışı durumu değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="2a04d-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="2a04d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a04d-120">-InputObject</span></span>
<span data-ttu-id="2a04d-121">Sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="2a04d-121">Certificate object</span></span>

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

### <span data-ttu-id="2a04d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a04d-122">-Name</span></span>
<span data-ttu-id="2a04d-123">Sertifika adı.</span><span class="sxs-lookup"><span data-stu-id="2a04d-123">Certificate name.</span></span>
<span data-ttu-id="2a04d-124">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a04d-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="2a04d-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2a04d-125">-PassThru</span></span>
<span data-ttu-id="2a04d-126">Cmdlet, varsayılan olarak nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="2a04d-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="2a04d-127">Bu anahtar belirtilmişse, sertifika nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a04d-127">If this switch is specified, return certificate object.</span></span>

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

### <span data-ttu-id="2a04d-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2a04d-128">-Tag</span></span>
<span data-ttu-id="2a04d-129">Sertifika etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="2a04d-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="2a04d-130">Belirtilmezse, var olan Etiketler değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="2a04d-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="2a04d-131">Boş bir Hashtable belirterek etiketi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2a04d-131">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="2a04d-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2a04d-132">-VaultName</span></span>
<span data-ttu-id="2a04d-133">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="2a04d-133">Vault name.</span></span>
<span data-ttu-id="2a04d-134">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a04d-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2a04d-135">-Version</span><span class="sxs-lookup"><span data-stu-id="2a04d-135">-Version</span></span>
<span data-ttu-id="2a04d-136">Sertifika sürümü.</span><span class="sxs-lookup"><span data-stu-id="2a04d-136">Certificate version.</span></span>
<span data-ttu-id="2a04d-137">Cmdlet, kasa adından bir sertifikanın FQDN 'sini, şu anda seçili ortamı, sertifika adını ve sertifika sürümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a04d-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

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

### <span data-ttu-id="2a04d-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="2a04d-138">-Confirm</span></span>
<span data-ttu-id="2a04d-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2a04d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a04d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a04d-140">-WhatIf</span></span>
<span data-ttu-id="2a04d-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a04d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a04d-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2a04d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a04d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a04d-143">CommonParameters</span></span>
<span data-ttu-id="2a04d-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a04d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a04d-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a04d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a04d-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a04d-146">INPUTS</span></span>

### <span data-ttu-id="2a04d-147">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="2a04d-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="2a04d-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a04d-148">OUTPUTS</span></span>

### <span data-ttu-id="2a04d-149">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2a04d-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="2a04d-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a04d-150">NOTES</span></span>

## <span data-ttu-id="2a04d-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a04d-151">RELATED LINKS</span></span>
