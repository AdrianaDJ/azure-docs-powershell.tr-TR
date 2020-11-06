---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594073"
---
# <span data-ttu-id="fc36e-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fc36e-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="fc36e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc36e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc36e-103">Sertifika bildirimleri için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="fc36e-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc36e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc36e-104">SYNTAX</span></span>

### <span data-ttu-id="fc36e-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc36e-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc36e-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="fc36e-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc36e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc36e-107">DESCRIPTION</span></span>
<span data-ttu-id="fc36e-108">**Add-AzureKeyVaultCertificateContact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki sertifika bildirimlerinin Anahtar Kasası için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="fc36e-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="fc36e-109">Kişi, sertifika bitiş tarihi, sertifika yenilenen gibi olaylarla ilgili güncelleştirmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="fc36e-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="fc36e-110">Bu olaylar sertifika ilkesi tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="fc36e-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="fc36e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc36e-111">EXAMPLES</span></span>

### <span data-ttu-id="fc36e-112">Örnek 1: Anahtar Kasası sertifikası kişisi ekleme</span><span class="sxs-lookup"><span data-stu-id="fc36e-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="fc36e-113">Bu komut ContosoKV01 Key Kasası için bir sertifika kişisi olarak Pat/ **KeyVaultCertificateContact**</span><span class="sxs-lookup"><span data-stu-id="fc36e-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="fc36e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc36e-114">PARAMETERS</span></span>

### <span data-ttu-id="fc36e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc36e-115">-DefaultProfile</span></span>
<span data-ttu-id="fc36e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fc36e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc36e-117">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="fc36e-117">-EmailAddress</span></span>
<span data-ttu-id="fc36e-118">Kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc36e-118">Specifies the email address of the contact.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc36e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc36e-119">-InputObject</span></span>
<span data-ttu-id="fc36e-120">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fc36e-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc36e-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fc36e-121">-PassThru</span></span>
<span data-ttu-id="fc36e-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc36e-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc36e-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fc36e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc36e-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fc36e-124">-VaultName</span></span>
<span data-ttu-id="fc36e-125">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc36e-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc36e-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc36e-126">-Confirm</span></span>
<span data-ttu-id="fc36e-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc36e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc36e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc36e-128">-WhatIf</span></span>
<span data-ttu-id="fc36e-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc36e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc36e-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc36e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc36e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc36e-131">CommonParameters</span></span>
<span data-ttu-id="fc36e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc36e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc36e-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc36e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc36e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc36e-134">INPUTS</span></span>

### <span data-ttu-id="fc36e-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fc36e-135">None</span></span>
<span data-ttu-id="fc36e-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fc36e-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc36e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc36e-137">OUTPUTS</span></span>

### <span data-ttu-id="fc36e-138">Liste<Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="fc36e-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="fc36e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc36e-139">NOTES</span></span>

## <span data-ttu-id="fc36e-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc36e-140">RELATED LINKS</span></span>

[<span data-ttu-id="fc36e-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fc36e-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="fc36e-142">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="fc36e-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

