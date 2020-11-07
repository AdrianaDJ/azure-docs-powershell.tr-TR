---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0b92fcb3725d42ac7c2978600f7903d6bf7f6142
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935781"
---
# <span data-ttu-id="116aa-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="116aa-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="116aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="116aa-102">SYNOPSIS</span></span>
<span data-ttu-id="116aa-103">Anahtar kasasından sertifika bildirimleri için kaydedilen bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="116aa-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="116aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="116aa-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="116aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="116aa-105">DESCRIPTION</span></span>
<span data-ttu-id="116aa-106">**Remove-AzKeyVaultCertificateContact** cmdlet 'i, bir anahtar kasasından sertifika bildirimleri için kaydedilmiş bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="116aa-106">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="116aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="116aa-107">EXAMPLES</span></span>

### <span data-ttu-id="116aa-108">Örnek 1: sertifika kişisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="116aa-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="116aa-109">Bu komut Contoso01 Key Kasası için bir sertifika kişisi olarak PATTI</span><span class="sxs-lookup"><span data-stu-id="116aa-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="116aa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="116aa-110">PARAMETERS</span></span>

### <span data-ttu-id="116aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116aa-111">-DefaultProfile</span></span>
<span data-ttu-id="116aa-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="116aa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="116aa-113">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="116aa-113">-EmailAddress</span></span>
<span data-ttu-id="116aa-114">Kaldırılacak kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="116aa-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="116aa-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="116aa-115">-PassThru</span></span>
<span data-ttu-id="116aa-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="116aa-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="116aa-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="116aa-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="116aa-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="116aa-118">-VaultName</span></span>
<span data-ttu-id="116aa-119">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="116aa-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="116aa-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="116aa-120">-Confirm</span></span>
<span data-ttu-id="116aa-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="116aa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="116aa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116aa-122">-WhatIf</span></span>
<span data-ttu-id="116aa-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="116aa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116aa-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="116aa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="116aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116aa-125">CommonParameters</span></span>
<span data-ttu-id="116aa-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="116aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116aa-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="116aa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116aa-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="116aa-128">INPUTS</span></span>

### <span data-ttu-id="116aa-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="116aa-129">None</span></span>
<span data-ttu-id="116aa-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="116aa-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="116aa-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="116aa-131">OUTPUTS</span></span>

### <span data-ttu-id="116aa-132">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="116aa-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="116aa-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="116aa-133">NOTES</span></span>

## <span data-ttu-id="116aa-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="116aa-134">RELATED LINKS</span></span>

[<span data-ttu-id="116aa-135">Add-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="116aa-135">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="116aa-136">Get-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="116aa-136">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

