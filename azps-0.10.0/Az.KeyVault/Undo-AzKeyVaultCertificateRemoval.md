---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 5757a9fb050d69cdf0ef0e648b0d446de1e3ee24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935767"
---
# <span data-ttu-id="d873e-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="d873e-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="d873e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d873e-102">SYNOPSIS</span></span>
<span data-ttu-id="d873e-103">Anahtar kasasındaki silinmiş sertifikayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="d873e-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="d873e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d873e-104">SYNTAX</span></span>

```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d873e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d873e-105">DESCRIPTION</span></span>
<span data-ttu-id="d873e-106">**Undo-Azanahtarvaultcertificateremoval** cmdlet 'i önceden silinmiş bir sertifikayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="d873e-106">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="d873e-107">Kurtarılan sertifika etkin olacak ve tüm işlemlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d873e-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="d873e-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d873e-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d873e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d873e-109">EXAMPLES</span></span>

### <span data-ttu-id="d873e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d873e-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="d873e-111">Bu komut, önceden silinmiş olan ' MyCertificate ' sertifikasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="d873e-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d873e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d873e-112">PARAMETERS</span></span>

### <span data-ttu-id="d873e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d873e-113">-DefaultProfile</span></span>
<span data-ttu-id="d873e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d873e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d873e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d873e-115">-Name</span></span>
<span data-ttu-id="d873e-116">Sertifika adı.</span><span class="sxs-lookup"><span data-stu-id="d873e-116">Certificate name.</span></span>
<span data-ttu-id="d873e-117">Cmdlet, kasa adından bir sertifikanın FQDN 'sini, şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d873e-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="d873e-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d873e-118">-VaultName</span></span>
<span data-ttu-id="d873e-119">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="d873e-119">Vault name.</span></span>
<span data-ttu-id="d873e-120">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d873e-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d873e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="d873e-121">-Confirm</span></span>
<span data-ttu-id="d873e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d873e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d873e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d873e-123">-WhatIf</span></span>
<span data-ttu-id="d873e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d873e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d873e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d873e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d873e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d873e-126">CommonParameters</span></span>
<span data-ttu-id="d873e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d873e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d873e-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d873e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d873e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d873e-129">INPUTS</span></span>

### <span data-ttu-id="d873e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d873e-130">System.String</span></span>

## <span data-ttu-id="d873e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d873e-131">OUTPUTS</span></span>

### <span data-ttu-id="d873e-132">Microsoft. Azure. Commands. Keykasa. modeller. Certificate</span><span class="sxs-lookup"><span data-stu-id="d873e-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="d873e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d873e-133">NOTES</span></span>

## <span data-ttu-id="d873e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d873e-134">RELATED LINKS</span></span>

[<span data-ttu-id="d873e-135">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d873e-135">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="d873e-136">Get-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="d873e-136">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
