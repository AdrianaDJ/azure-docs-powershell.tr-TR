---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 1fbf5a5541fe3e1360e696f9c06a26d6ea131dc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593560"
---
# <span data-ttu-id="0fe03-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0fe03-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="0fe03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe03-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe03-103">Anahtar kasasından sertifika bildirimleri için kaydedilen bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="0fe03-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fe03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fe03-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe03-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fe03-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe03-106">**Remove-AzureKeyVaultCertificateContact** cmdlet 'i, anahtar kasadan gelen sertifika bildirimleri için kaydedilmiş bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="0fe03-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="0fe03-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fe03-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe03-108">Örnek 1: sertifika kişisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0fe03-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="0fe03-109">Bu komut Contoso01 Key Kasası için bir sertifika kişisi olarak PATTI</span><span class="sxs-lookup"><span data-stu-id="0fe03-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="0fe03-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fe03-110">PARAMETERS</span></span>

### <span data-ttu-id="0fe03-111">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="0fe03-111">-EmailAddress</span></span>
<span data-ttu-id="0fe03-112">Kaldırılacak kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fe03-112">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe03-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0fe03-113">-PassThru</span></span>
<span data-ttu-id="0fe03-114">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0fe03-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0fe03-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0fe03-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0fe03-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0fe03-116">-VaultName</span></span>
<span data-ttu-id="0fe03-117">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fe03-117">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="0fe03-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="0fe03-118">-Confirm</span></span>
<span data-ttu-id="0fe03-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0fe03-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe03-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe03-120">-WhatIf</span></span>
<span data-ttu-id="0fe03-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fe03-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe03-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0fe03-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe03-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe03-123">-DefaultProfile</span></span>
<span data-ttu-id="0fe03-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0fe03-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fe03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe03-125">CommonParameters</span></span>
<span data-ttu-id="0fe03-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fe03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe03-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe03-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe03-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fe03-128">INPUTS</span></span>

## <span data-ttu-id="0fe03-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fe03-129">OUTPUTS</span></span>

### <span data-ttu-id="0fe03-130">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="0fe03-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="0fe03-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fe03-131">NOTES</span></span>

## <span data-ttu-id="0fe03-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fe03-132">RELATED LINKS</span></span>

[<span data-ttu-id="0fe03-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0fe03-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="0fe03-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0fe03-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

