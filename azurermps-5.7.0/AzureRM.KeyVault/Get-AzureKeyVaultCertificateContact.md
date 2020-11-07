---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: cf60626ec04a2466fc9565aef5daff896281345d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762370"
---
# <span data-ttu-id="846e8-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="846e8-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="846e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="846e8-102">SYNOPSIS</span></span>
<span data-ttu-id="846e8-103">Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="846e8-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="846e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="846e8-104">SYNTAX</span></span>

### <span data-ttu-id="846e8-105">VaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="846e8-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="846e8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="846e8-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="846e8-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="846e8-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="846e8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="846e8-108">DESCRIPTION</span></span>
<span data-ttu-id="846e8-109">**Get-AzureKeyVaultCertificateContact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="846e8-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="846e8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="846e8-110">EXAMPLES</span></span>

### <span data-ttu-id="846e8-111">Örnek 1: tüm sertifika kişilerini alma</span><span class="sxs-lookup"><span data-stu-id="846e8-111">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="846e8-112">Bu komut contoso tuş Kasası 'ndaki sertifika nesneleri için tüm kişileri alır ve $Contacts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="846e8-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="846e8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="846e8-113">PARAMETERS</span></span>

### <span data-ttu-id="846e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="846e8-114">-DefaultProfile</span></span>
<span data-ttu-id="846e8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="846e8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="846e8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="846e8-116">-InputObject</span></span>
<span data-ttu-id="846e8-117">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="846e8-117">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="846e8-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="846e8-118">-ResourceId</span></span>
<span data-ttu-id="846e8-119">Tuş Kasası kimliği.</span><span class="sxs-lookup"><span data-stu-id="846e8-119">KeyVault Id.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846e8-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="846e8-120">-VaultName</span></span>
<span data-ttu-id="846e8-121">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="846e8-121">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="846e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="846e8-122">CommonParameters</span></span>
<span data-ttu-id="846e8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="846e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="846e8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="846e8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="846e8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="846e8-125">INPUTS</span></span>

### <span data-ttu-id="846e8-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="846e8-126">None</span></span>
<span data-ttu-id="846e8-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="846e8-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="846e8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="846e8-128">OUTPUTS</span></span>

### <span data-ttu-id="846e8-129">Liste<Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="846e8-129">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="846e8-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="846e8-130">NOTES</span></span>

## <span data-ttu-id="846e8-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="846e8-131">RELATED LINKS</span></span>

[<span data-ttu-id="846e8-132">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="846e8-132">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="846e8-133">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="846e8-133">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

