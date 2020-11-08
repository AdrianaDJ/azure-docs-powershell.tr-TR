---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096628"
---
# <span data-ttu-id="15bfd-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="15bfd-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="15bfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="15bfd-103">Sertifika bildirimleri için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="15bfd-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="15bfd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15bfd-104">SYNTAX</span></span>

### <span data-ttu-id="15bfd-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15bfd-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15bfd-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="15bfd-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15bfd-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="15bfd-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15bfd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="15bfd-108">DESCRIPTION</span></span>
<span data-ttu-id="15bfd-109">**Add-Azanahtarvaultcertificatecontact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki sertifika bildirimlerinin Anahtar Kasası için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="15bfd-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="15bfd-110">Kişi, sertifika bitiş tarihi, sertifika yenilenen gibi olaylarla ilgili güncelleştirmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="15bfd-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="15bfd-111">Bu olaylar sertifika ilkesi tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="15bfd-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="15bfd-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15bfd-112">EXAMPLES</span></span>

### <span data-ttu-id="15bfd-113">Örnek 1: Anahtar Kasası sertifikası kişisi ekleme</span><span class="sxs-lookup"><span data-stu-id="15bfd-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="15bfd-114">Bu komut, ContosoKV01 Key Kasası için bir sertifika kişisi olarak PATTI güneş ekler ve "ContosoKV01" Kasası için kişi listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="15bfd-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="15bfd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15bfd-115">PARAMETERS</span></span>

### <span data-ttu-id="15bfd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bfd-116">-DefaultProfile</span></span>
<span data-ttu-id="15bfd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="15bfd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15bfd-118">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="15bfd-118">-EmailAddress</span></span>
<span data-ttu-id="15bfd-119">Kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15bfd-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bfd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15bfd-120">-InputObject</span></span>
<span data-ttu-id="15bfd-121">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="15bfd-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15bfd-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="15bfd-122">-PassThru</span></span>
<span data-ttu-id="15bfd-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="15bfd-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="15bfd-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="15bfd-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15bfd-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="15bfd-125">-ResourceId</span></span>
<span data-ttu-id="15bfd-126">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="15bfd-126">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bfd-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="15bfd-127">-VaultName</span></span>
<span data-ttu-id="15bfd-128">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15bfd-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15bfd-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="15bfd-129">-Confirm</span></span>
<span data-ttu-id="15bfd-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15bfd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15bfd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15bfd-131">-WhatIf</span></span>
<span data-ttu-id="15bfd-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15bfd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15bfd-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15bfd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15bfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bfd-134">CommonParameters</span></span>
<span data-ttu-id="15bfd-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15bfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bfd-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15bfd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bfd-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15bfd-137">INPUTS</span></span>

### <span data-ttu-id="15bfd-138">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="15bfd-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="15bfd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="15bfd-139">System.String</span></span>

## <span data-ttu-id="15bfd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15bfd-140">OUTPUTS</span></span>

### <span data-ttu-id="15bfd-141">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="15bfd-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="15bfd-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15bfd-142">NOTES</span></span>

## <span data-ttu-id="15bfd-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15bfd-143">RELATED LINKS</span></span>

[<span data-ttu-id="15bfd-144">Get-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="15bfd-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="15bfd-145">Remove-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="15bfd-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)
