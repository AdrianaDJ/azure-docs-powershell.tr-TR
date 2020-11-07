---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9bfb62388ce4a7a8994f4a618a4c1a00ac5868d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938841"
---
# <span data-ttu-id="4e6ee-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4e6ee-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="4e6ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6ee-103">Anahtar kasasından sertifika bildirimleri için kaydedilen bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e6ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e6ee-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e6ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e6ee-105">DESCRIPTION</span></span>
<span data-ttu-id="4e6ee-106">**Remove-AzureKeyVaultCertificateContact** cmdlet 'i, anahtar kasadan gelen sertifika bildirimleri için kaydedilmiş bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="4e6ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e6ee-107">EXAMPLES</span></span>

### <span data-ttu-id="4e6ee-108">Örnek 1: sertifika kişisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4e6ee-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="4e6ee-109">Bu komut Contoso01 Key Kasası için bir sertifika kişisi olarak PATTI</span><span class="sxs-lookup"><span data-stu-id="4e6ee-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="4e6ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e6ee-110">PARAMETERS</span></span>

### <span data-ttu-id="4e6ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6ee-111">-DefaultProfile</span></span>
<span data-ttu-id="4e6ee-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4e6ee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e6ee-113">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="4e6ee-113">-EmailAddress</span></span>
<span data-ttu-id="4e6ee-114">Kaldırılacak kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6ee-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4e6ee-115">-PassThru</span></span>
<span data-ttu-id="4e6ee-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4e6ee-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4e6ee-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4e6ee-118">-VaultName</span></span>
<span data-ttu-id="4e6ee-119">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4e6ee-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e6ee-120">-Confirm</span></span>
<span data-ttu-id="4e6ee-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e6ee-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e6ee-122">-WhatIf</span></span>
<span data-ttu-id="4e6ee-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e6ee-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e6ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6ee-125">CommonParameters</span></span>
<span data-ttu-id="4e6ee-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e6ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6ee-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e6ee-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6ee-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e6ee-128">INPUTS</span></span>

## <span data-ttu-id="4e6ee-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e6ee-129">OUTPUTS</span></span>

### <span data-ttu-id="4e6ee-130">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="4e6ee-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="4e6ee-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e6ee-131">NOTES</span></span>

## <span data-ttu-id="4e6ee-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e6ee-132">RELATED LINKS</span></span>

[<span data-ttu-id="4e6ee-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4e6ee-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="4e6ee-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4e6ee-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

