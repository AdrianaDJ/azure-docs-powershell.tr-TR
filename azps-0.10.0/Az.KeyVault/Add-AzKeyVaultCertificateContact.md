---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936680"
---
# <span data-ttu-id="b6346-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b6346-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b6346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6346-102">SYNOPSIS</span></span>
<span data-ttu-id="b6346-103">Sertifika bildirimleri için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="b6346-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="b6346-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6346-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6346-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6346-105">DESCRIPTION</span></span>
<span data-ttu-id="b6346-106">**Add-Azanahtarvaultcertificatecontact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki sertifika bildirimlerinin Anahtar Kasası için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="b6346-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="b6346-107">Kişi, sertifika bitiş tarihi, sertifika yenilenen gibi olaylarla ilgili güncelleştirmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="b6346-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="b6346-108">Bu olaylar sertifika ilkesi tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="b6346-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="b6346-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6346-109">EXAMPLES</span></span>

### <span data-ttu-id="b6346-110">Örnek 1: Anahtar Kasası sertifikası kişisi ekleme</span><span class="sxs-lookup"><span data-stu-id="b6346-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="b6346-111">Bu komut ContosoKV01 Key Kasası için bir sertifika kişisi olarak Pat/ **KeyVaultCertificateContact**</span><span class="sxs-lookup"><span data-stu-id="b6346-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="b6346-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6346-112">PARAMETERS</span></span>

### <span data-ttu-id="b6346-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6346-113">-DefaultProfile</span></span>
<span data-ttu-id="b6346-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b6346-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6346-115">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="b6346-115">-EmailAddress</span></span>
<span data-ttu-id="b6346-116">Kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6346-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="b6346-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b6346-117">-PassThru</span></span>
<span data-ttu-id="b6346-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b6346-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b6346-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b6346-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6346-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b6346-120">-VaultName</span></span>
<span data-ttu-id="b6346-121">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6346-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="b6346-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6346-122">-Confirm</span></span>
<span data-ttu-id="b6346-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6346-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6346-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6346-124">-WhatIf</span></span>
<span data-ttu-id="b6346-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6346-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6346-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6346-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6346-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6346-127">CommonParameters</span></span>
<span data-ttu-id="b6346-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6346-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6346-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6346-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6346-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6346-130">INPUTS</span></span>

### <span data-ttu-id="b6346-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b6346-131">None</span></span>
<span data-ttu-id="b6346-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b6346-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6346-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6346-133">OUTPUTS</span></span>

### <span data-ttu-id="b6346-134">Liste<Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="b6346-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="b6346-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6346-135">NOTES</span></span>

## <span data-ttu-id="b6346-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6346-136">RELATED LINKS</span></span>

[<span data-ttu-id="b6346-137">Get-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="b6346-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="b6346-138">Remove-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="b6346-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)
