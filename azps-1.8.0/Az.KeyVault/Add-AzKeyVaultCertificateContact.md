---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ff363ae1bf6581baaeb177edd4e215494c82f85f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916383"
---
# <span data-ttu-id="52d77-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="52d77-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="52d77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d77-102">SYNOPSIS</span></span>
<span data-ttu-id="52d77-103">Sertifika bildirimleri için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="52d77-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="52d77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52d77-104">SYNTAX</span></span>

### <span data-ttu-id="52d77-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52d77-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d77-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="52d77-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52d77-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="52d77-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52d77-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="52d77-108">DESCRIPTION</span></span>
<span data-ttu-id="52d77-109">**Add-Azanahtarvaultcertificatecontact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki sertifika bildirimlerinin Anahtar Kasası için bir kişi ekler.</span><span class="sxs-lookup"><span data-stu-id="52d77-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="52d77-110">Kişi, sertifika bitiş tarihi, sertifika yenilenen gibi olaylarla ilgili güncelleştirmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="52d77-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="52d77-111">Bu olaylar sertifika ilkesi tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="52d77-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="52d77-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52d77-112">EXAMPLES</span></span>

### <span data-ttu-id="52d77-113">Örnek 1: Anahtar Kasası sertifikası kişisi ekleme</span><span class="sxs-lookup"><span data-stu-id="52d77-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="52d77-114">Bu komut, ContosoKV01 Key Kasası için bir sertifika kişisi olarak PATTI güneş ekler ve "ContosoKV01" Kasası için kişi listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="52d77-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="52d77-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52d77-115">PARAMETERS</span></span>

### <span data-ttu-id="52d77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d77-116">-DefaultProfile</span></span>
<span data-ttu-id="52d77-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52d77-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52d77-118">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="52d77-118">-EmailAddress</span></span>
<span data-ttu-id="52d77-119">Kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d77-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="52d77-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52d77-120">-InputObject</span></span>
<span data-ttu-id="52d77-121">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="52d77-121">KeyVault object.</span></span>

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

### <span data-ttu-id="52d77-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="52d77-122">-PassThru</span></span>
<span data-ttu-id="52d77-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="52d77-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52d77-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="52d77-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52d77-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="52d77-125">-ResourceId</span></span>
<span data-ttu-id="52d77-126">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="52d77-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="52d77-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="52d77-127">-VaultName</span></span>
<span data-ttu-id="52d77-128">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d77-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="52d77-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="52d77-129">-Confirm</span></span>
<span data-ttu-id="52d77-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52d77-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52d77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d77-131">-WhatIf</span></span>
<span data-ttu-id="52d77-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52d77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52d77-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52d77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52d77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d77-134">CommonParameters</span></span>
<span data-ttu-id="52d77-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52d77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d77-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d77-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d77-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52d77-137">INPUTS</span></span>

### <span data-ttu-id="52d77-138">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="52d77-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="52d77-139">System. String</span><span class="sxs-lookup"><span data-stu-id="52d77-139">System.String</span></span>

## <span data-ttu-id="52d77-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52d77-140">OUTPUTS</span></span>

### <span data-ttu-id="52d77-141">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="52d77-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="52d77-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52d77-142">NOTES</span></span>

## <span data-ttu-id="52d77-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52d77-143">RELATED LINKS</span></span>

[<span data-ttu-id="52d77-144">Get-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="52d77-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="52d77-145">Remove-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="52d77-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

