---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: aee18adf3530976af4b17ffa15f94624248a7db7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590234"
---
# <span data-ttu-id="47d1b-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="47d1b-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="47d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="47d1b-103">Anahtar kasasından sertifika bildirimleri için kaydedilen bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="47d1b-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47d1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47d1b-104">SYNTAX</span></span>

### <span data-ttu-id="47d1b-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47d1b-105">ByName (Default)</span></span>
```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47d1b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="47d1b-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47d1b-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="47d1b-107">ByResourceId</span></span>
```
Remove-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47d1b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47d1b-108">DESCRIPTION</span></span>
<span data-ttu-id="47d1b-109">**Remove-AzureKeyVaultCertificateContact** cmdlet 'i, anahtar kasadan gelen sertifika bildirimleri için kaydedilmiş bir kişiyi siler.</span><span class="sxs-lookup"><span data-stu-id="47d1b-109">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="47d1b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47d1b-110">EXAMPLES</span></span>

### <span data-ttu-id="47d1b-111">Örnek 1: sertifika kişisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="47d1b-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="47d1b-112">Bu komut Contoso01 Key Kasası için bir sertifika kişisi olarak PATTI</span><span class="sxs-lookup"><span data-stu-id="47d1b-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="47d1b-113">Geçiş belirtildiyse, cmdlet kalan sertifika kişilerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="47d1b-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="47d1b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47d1b-114">PARAMETERS</span></span>

### <span data-ttu-id="47d1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d1b-115">-DefaultProfile</span></span>
<span data-ttu-id="47d1b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="47d1b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47d1b-117">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="47d1b-117">-EmailAddress</span></span>
<span data-ttu-id="47d1b-118">Kaldırılacak kişinin e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47d1b-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="47d1b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47d1b-119">-InputObject</span></span>
<span data-ttu-id="47d1b-120">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="47d1b-120">KeyVault object.</span></span>

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

### <span data-ttu-id="47d1b-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="47d1b-121">-PassThru</span></span>
<span data-ttu-id="47d1b-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="47d1b-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="47d1b-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="47d1b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="47d1b-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="47d1b-124">-ResourceId</span></span>
<span data-ttu-id="47d1b-125">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="47d1b-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="47d1b-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="47d1b-126">-VaultName</span></span>
<span data-ttu-id="47d1b-127">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47d1b-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="47d1b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="47d1b-128">-Confirm</span></span>
<span data-ttu-id="47d1b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47d1b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47d1b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47d1b-130">-WhatIf</span></span>
<span data-ttu-id="47d1b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47d1b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47d1b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47d1b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47d1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d1b-133">CommonParameters</span></span>
<span data-ttu-id="47d1b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47d1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d1b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47d1b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d1b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47d1b-136">INPUTS</span></span>

### <span data-ttu-id="47d1b-137">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="47d1b-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="47d1b-138">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="47d1b-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="47d1b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="47d1b-139">System.String</span></span>

## <span data-ttu-id="47d1b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47d1b-140">OUTPUTS</span></span>

### <span data-ttu-id="47d1b-141">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="47d1b-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="47d1b-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47d1b-142">NOTES</span></span>

## <span data-ttu-id="47d1b-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47d1b-143">RELATED LINKS</span></span>

[<span data-ttu-id="47d1b-144">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="47d1b-144">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="47d1b-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="47d1b-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

