---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939367"
---
# <span data-ttu-id="45b49-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="45b49-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="45b49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45b49-102">SYNOPSIS</span></span>
<span data-ttu-id="45b49-103">Anahtar kasasındaki silinmiş sertifikayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="45b49-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45b49-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b49-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45b49-105">DESCRIPTION</span></span>
<span data-ttu-id="45b49-106">**Undo-AzureKeyVaultCertificateRemoval** cmdlet 'i önceden silinmiş bir sertifikayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="45b49-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="45b49-107">Kurtarılan sertifika etkin olacak ve tüm işlemlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="45b49-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="45b49-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="45b49-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="45b49-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45b49-109">EXAMPLES</span></span>

### <span data-ttu-id="45b49-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="45b49-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="45b49-111">Bu komut, önceden silinmiş olan ' MyCertificate ' sertifikasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="45b49-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="45b49-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45b49-112">PARAMETERS</span></span>

### <span data-ttu-id="45b49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b49-113">-DefaultProfile</span></span>
<span data-ttu-id="45b49-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="45b49-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45b49-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="45b49-115">-Name</span></span>
<span data-ttu-id="45b49-116">Sertifika adı.</span><span class="sxs-lookup"><span data-stu-id="45b49-116">Certificate name.</span></span>
<span data-ttu-id="45b49-117">Cmdlet, kasa adından bir sertifikanın FQDN 'sini, şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45b49-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45b49-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="45b49-118">-VaultName</span></span>
<span data-ttu-id="45b49-119">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="45b49-119">Vault name.</span></span>
<span data-ttu-id="45b49-120">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45b49-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="45b49-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="45b49-121">-Confirm</span></span>
<span data-ttu-id="45b49-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45b49-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b49-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b49-123">-WhatIf</span></span>
<span data-ttu-id="45b49-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45b49-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45b49-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="45b49-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b49-126">CommonParameters</span></span>
<span data-ttu-id="45b49-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45b49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b49-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b49-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b49-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45b49-129">INPUTS</span></span>

### <span data-ttu-id="45b49-130">System. String</span><span class="sxs-lookup"><span data-stu-id="45b49-130">System.String</span></span>

## <span data-ttu-id="45b49-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45b49-131">OUTPUTS</span></span>

### <span data-ttu-id="45b49-132">Microsoft. Azure. Commands. Keykasa. modeller. Certificate</span><span class="sxs-lookup"><span data-stu-id="45b49-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="45b49-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45b49-133">NOTES</span></span>

## <span data-ttu-id="45b49-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45b49-134">RELATED LINKS</span></span>

[<span data-ttu-id="45b49-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="45b49-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="45b49-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="45b49-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
