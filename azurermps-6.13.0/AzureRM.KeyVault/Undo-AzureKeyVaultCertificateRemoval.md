---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: db2b9066524bd21daa1fa65b87554d9b028754de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594405"
---
# <span data-ttu-id="b429a-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="b429a-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="b429a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b429a-102">SYNOPSIS</span></span>
<span data-ttu-id="b429a-103">Anahtar kasasındaki silinmiş sertifikayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="b429a-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b429a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b429a-104">SYNTAX</span></span>

### <span data-ttu-id="b429a-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b429a-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b429a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b429a-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b429a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b429a-107">DESCRIPTION</span></span>
<span data-ttu-id="b429a-108">**Undo-AzureKeyVaultCertificateRemoval** cmdlet 'i önceden silinmiş bir sertifikayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="b429a-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="b429a-109">Kurtarılan sertifika etkin olacak ve tüm işlemlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b429a-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="b429a-110">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b429a-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b429a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b429a-111">EXAMPLES</span></span>

### <span data-ttu-id="b429a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b429a-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="b429a-113">Bu komut, önceden silinmiş olan ' MyCertificate ' sertifikasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="b429a-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b429a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b429a-114">PARAMETERS</span></span>

### <span data-ttu-id="b429a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b429a-115">-DefaultProfile</span></span>
<span data-ttu-id="b429a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b429a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b429a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b429a-117">-InputObject</span></span>
<span data-ttu-id="b429a-118">Silinmiş sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="b429a-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b429a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b429a-119">-Name</span></span>
<span data-ttu-id="b429a-120">Sertifika adı.</span><span class="sxs-lookup"><span data-stu-id="b429a-120">Certificate name.</span></span>
<span data-ttu-id="b429a-121">Cmdlet, kasa adından bir sertifikanın FQDN 'sini, şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b429a-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b429a-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b429a-122">-VaultName</span></span>
<span data-ttu-id="b429a-123">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="b429a-123">Vault name.</span></span>
<span data-ttu-id="b429a-124">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b429a-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b429a-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b429a-125">-Confirm</span></span>
<span data-ttu-id="b429a-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b429a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b429a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b429a-127">-WhatIf</span></span>
<span data-ttu-id="b429a-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b429a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b429a-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b429a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b429a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b429a-130">CommonParameters</span></span>
<span data-ttu-id="b429a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b429a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b429a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b429a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b429a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b429a-133">INPUTS</span></span>

### <span data-ttu-id="b429a-134">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="b429a-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="b429a-135">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b429a-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b429a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b429a-136">OUTPUTS</span></span>

### <span data-ttu-id="b429a-137">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b429a-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="b429a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b429a-138">NOTES</span></span>

## <span data-ttu-id="b429a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b429a-139">RELATED LINKS</span></span>

[<span data-ttu-id="b429a-140">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b429a-140">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="b429a-141">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b429a-141">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
