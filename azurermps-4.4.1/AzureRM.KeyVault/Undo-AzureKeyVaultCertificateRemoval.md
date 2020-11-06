---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 91fee65a201de8babc7ef7aa09973f1e98f95cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594244"
---
# <span data-ttu-id="fa0fb-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="fa0fb-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="fa0fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa0fb-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0fb-103">Anahtar kasasındaki silinmiş sertifikayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa0fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa0fb-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa0fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa0fb-105">DESCRIPTION</span></span>
<span data-ttu-id="fa0fb-106">**Undo-AzureKeyVaultCertificateRemoval** cmdlet 'i önceden silinmiş bir sertifikayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="fa0fb-107">Kurtarılan sertifika etkin olacak ve tüm işlemlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="fa0fb-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="fa0fb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa0fb-109">EXAMPLES</span></span>

### <span data-ttu-id="fa0fb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fa0fb-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="fa0fb-111">Bu komut, önceden silinmiş olan ' MyCertificate ' sertifikasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="fa0fb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa0fb-112">PARAMETERS</span></span>

### <span data-ttu-id="fa0fb-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa0fb-113">-Name</span></span>
<span data-ttu-id="fa0fb-114">Sertifika adı.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-114">Certificate name.</span></span>
<span data-ttu-id="fa0fb-115">Cmdlet, kasa adından bir sertifikanın FQDN 'sini, şu anda seçili olan ortamı ve sertifika adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-115">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0fb-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fa0fb-116">-VaultName</span></span>
<span data-ttu-id="fa0fb-117">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-117">Vault name.</span></span>
<span data-ttu-id="fa0fb-118">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0fb-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa0fb-119">-Confirm</span></span>
<span data-ttu-id="fa0fb-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0fb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0fb-121">-WhatIf</span></span>
<span data-ttu-id="fa0fb-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0fb-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0fb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0fb-124">-DefaultProfile</span></span>
<span data-ttu-id="fa0fb-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa0fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0fb-126">CommonParameters</span></span>
<span data-ttu-id="fa0fb-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa0fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0fb-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa0fb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0fb-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa0fb-129">INPUTS</span></span>

### <span data-ttu-id="fa0fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fa0fb-130">System.String</span></span>

## <span data-ttu-id="fa0fb-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa0fb-131">OUTPUTS</span></span>

### <span data-ttu-id="fa0fb-132">Microsoft. Azure. Commands. Keykasa. modeller. Certificate</span><span class="sxs-lookup"><span data-stu-id="fa0fb-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="fa0fb-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa0fb-133">NOTES</span></span>

## <span data-ttu-id="fa0fb-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa0fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="fa0fb-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fa0fb-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="fa0fb-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fa0fb-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
