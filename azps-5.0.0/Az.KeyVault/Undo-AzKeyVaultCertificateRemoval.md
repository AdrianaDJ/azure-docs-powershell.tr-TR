---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319882"
---
# <span data-ttu-id="fb920-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="fb920-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="fb920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb920-102">SYNOPSIS</span></span>
<span data-ttu-id="fb920-103">Anahtar kasasındaki silinmiş sertifikayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fb920-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="fb920-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb920-104">SYNTAX</span></span>

### <span data-ttu-id="fb920-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb920-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb920-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fb920-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb920-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb920-107">DESCRIPTION</span></span>
<span data-ttu-id="fb920-108">**Undo-Azanahtarvaultcertificateremoval** cmdlet 'i önceden silinmiş bir sertifikayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fb920-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="fb920-109">Kurtarılan sertifika etkin olacak ve tüm işlemlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fb920-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="fb920-110">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb920-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="fb920-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb920-111">EXAMPLES</span></span>

### <span data-ttu-id="fb920-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb920-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

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

<span data-ttu-id="fb920-113">Bu komut, önceden silinmiş olan ' MyCertificate ' sertifikasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fb920-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="fb920-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb920-114">PARAMETERS</span></span>

### <span data-ttu-id="fb920-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb920-115">-DefaultProfile</span></span>
<span data-ttu-id="fb920-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fb920-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb920-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb920-117">-InputObject</span></span>
<span data-ttu-id="fb920-118">Silinmiş sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="fb920-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="fb920-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb920-119">-Name</span></span>
<span data-ttu-id="fb920-120">Sertifika adı.</span><span class="sxs-lookup"><span data-stu-id="fb920-120">Certificate name.</span></span>
<span data-ttu-id="fb920-121">Cmdlet, kasa adından bir sertifikanın FQDN 'sini, şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb920-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="fb920-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fb920-122">-VaultName</span></span>
<span data-ttu-id="fb920-123">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="fb920-123">Vault name.</span></span>
<span data-ttu-id="fb920-124">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb920-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fb920-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb920-125">-Confirm</span></span>
<span data-ttu-id="fb920-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb920-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb920-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb920-127">-WhatIf</span></span>
<span data-ttu-id="fb920-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb920-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb920-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb920-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb920-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb920-130">CommonParameters</span></span>
<span data-ttu-id="fb920-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb920-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb920-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fb920-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb920-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb920-133">INPUTS</span></span>

### <span data-ttu-id="fb920-134">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="fb920-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="fb920-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb920-135">OUTPUTS</span></span>

### <span data-ttu-id="fb920-136">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fb920-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="fb920-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb920-137">NOTES</span></span>

## <span data-ttu-id="fb920-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb920-138">RELATED LINKS</span></span>

[<span data-ttu-id="fb920-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fb920-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="fb920-140">Get-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="fb920-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
