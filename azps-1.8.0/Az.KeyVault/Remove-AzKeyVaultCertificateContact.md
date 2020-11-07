---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0f1768bec11c5a85e97cdb27e6e9a3195c3880b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916280"
---
# <span data-ttu-id="04c88-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="04c88-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="04c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04c88-102">SYNOPSIS</span></span>
<span data-ttu-id="04c88-103">Anahtar kasasından sertifika bildirimleri için kaydedilen bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="04c88-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="04c88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04c88-104">SYNTAX</span></span>

### <span data-ttu-id="04c88-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04c88-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04c88-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="04c88-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04c88-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="04c88-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04c88-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="04c88-108">DESCRIPTION</span></span>
<span data-ttu-id="04c88-109">**Remove-AzKeyVaultCertificateContact** cmdlet 'i, bir anahtar kasasından sertifika bildirimleri için kaydedilmiş bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="04c88-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="04c88-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04c88-110">EXAMPLES</span></span>

### <span data-ttu-id="04c88-111">Örnek 1: sertifika kişisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="04c88-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="04c88-112">Bu komut Contoso01 Key Kasası için bir sertifika kişisi olarak PATTI</span><span class="sxs-lookup"><span data-stu-id="04c88-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="04c88-113">Geçiş belirtildiyse, cmdlet kalan sertifika kişilerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="04c88-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="04c88-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04c88-114">PARAMETERS</span></span>

### <span data-ttu-id="04c88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c88-115">-DefaultProfile</span></span>
<span data-ttu-id="04c88-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="04c88-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04c88-117">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="04c88-117">-EmailAddress</span></span>
<span data-ttu-id="04c88-118">Kaldırılacak kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04c88-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="04c88-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04c88-119">-InputObject</span></span>
<span data-ttu-id="04c88-120">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="04c88-120">KeyVault object.</span></span>

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

### <span data-ttu-id="04c88-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="04c88-121">-PassThru</span></span>
<span data-ttu-id="04c88-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="04c88-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="04c88-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="04c88-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04c88-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="04c88-124">-ResourceId</span></span>
<span data-ttu-id="04c88-125">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="04c88-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="04c88-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="04c88-126">-VaultName</span></span>
<span data-ttu-id="04c88-127">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04c88-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c88-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="04c88-128">-Confirm</span></span>
<span data-ttu-id="04c88-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04c88-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c88-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c88-130">-WhatIf</span></span>
<span data-ttu-id="04c88-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04c88-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04c88-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04c88-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c88-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c88-133">CommonParameters</span></span>
<span data-ttu-id="04c88-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04c88-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c88-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04c88-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c88-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04c88-136">INPUTS</span></span>

### <span data-ttu-id="04c88-137">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="04c88-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="04c88-138">System. String</span><span class="sxs-lookup"><span data-stu-id="04c88-138">System.String</span></span>

## <span data-ttu-id="04c88-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04c88-139">OUTPUTS</span></span>

### <span data-ttu-id="04c88-140">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="04c88-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="04c88-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04c88-141">NOTES</span></span>

## <span data-ttu-id="04c88-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04c88-142">RELATED LINKS</span></span>

[<span data-ttu-id="04c88-143">Add-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="04c88-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="04c88-144">Get-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="04c88-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

