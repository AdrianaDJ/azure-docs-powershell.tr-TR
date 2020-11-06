---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594259"
---
# <span data-ttu-id="f022b-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f022b-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="f022b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f022b-102">SYNOPSIS</span></span>
<span data-ttu-id="f022b-103">Sertifika bildirimleri için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="f022b-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f022b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f022b-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f022b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f022b-105">DESCRIPTION</span></span>
<span data-ttu-id="f022b-106">**Add-AzureKeyVaultCertificateContact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki sertifika bildirimlerinin Anahtar Kasası için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="f022b-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="f022b-107">Kişi, sertifika bitiş tarihi, sertifika yenilenen gibi olaylarla ilgili güncelleştirmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="f022b-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="f022b-108">Bu olaylar sertifika ilkesi tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="f022b-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="f022b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f022b-109">EXAMPLES</span></span>

### <span data-ttu-id="f022b-110">Örnek 1: Anahtar Kasası sertifikası kişisi ekleme</span><span class="sxs-lookup"><span data-stu-id="f022b-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="f022b-111">Bu komut ContosoKV01 Key Kasası için bir sertifika kişisi olarak Pat/ **KeyVaultCertificateContact**</span><span class="sxs-lookup"><span data-stu-id="f022b-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="f022b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f022b-112">PARAMETERS</span></span>

### <span data-ttu-id="f022b-113">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="f022b-113">-EmailAddress</span></span>
<span data-ttu-id="f022b-114">Kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f022b-114">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="f022b-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f022b-115">-PassThru</span></span>
<span data-ttu-id="f022b-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f022b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f022b-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f022b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f022b-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f022b-118">-VaultName</span></span>
<span data-ttu-id="f022b-119">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f022b-119">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="f022b-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="f022b-120">-Confirm</span></span>
<span data-ttu-id="f022b-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f022b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f022b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f022b-122">-WhatIf</span></span>
<span data-ttu-id="f022b-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f022b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f022b-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f022b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f022b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f022b-125">-DefaultProfile</span></span>
<span data-ttu-id="f022b-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f022b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f022b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f022b-127">CommonParameters</span></span>
<span data-ttu-id="f022b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f022b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f022b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f022b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f022b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f022b-130">INPUTS</span></span>

## <span data-ttu-id="f022b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f022b-131">OUTPUTS</span></span>

### <span data-ttu-id="f022b-132">Liste<Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="f022b-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="f022b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f022b-133">NOTES</span></span>

## <span data-ttu-id="f022b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f022b-134">RELATED LINKS</span></span>

[<span data-ttu-id="f022b-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f022b-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="f022b-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="f022b-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

