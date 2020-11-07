---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935805"
---
# <span data-ttu-id="e2eab-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e2eab-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e2eab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2eab-102">SYNOPSIS</span></span>
<span data-ttu-id="e2eab-103">Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="e2eab-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="e2eab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2eab-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2eab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2eab-105">DESCRIPTION</span></span>
<span data-ttu-id="e2eab-106">**Get-Azanahtarvaultcertificatecontact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="e2eab-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="e2eab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2eab-107">EXAMPLES</span></span>

### <span data-ttu-id="e2eab-108">Örnek 1: tüm sertifika kişilerini alma</span><span class="sxs-lookup"><span data-stu-id="e2eab-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="e2eab-109">Bu komut contoso tuş Kasası 'ndaki sertifika nesneleri için tüm kişileri alır ve $Contacts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e2eab-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="e2eab-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2eab-110">PARAMETERS</span></span>

### <span data-ttu-id="e2eab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2eab-111">-DefaultProfile</span></span>
<span data-ttu-id="e2eab-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e2eab-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2eab-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e2eab-113">-VaultName</span></span>
<span data-ttu-id="e2eab-114">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2eab-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="e2eab-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2eab-115">CommonParameters</span></span>
<span data-ttu-id="e2eab-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2eab-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2eab-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2eab-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2eab-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2eab-118">INPUTS</span></span>

### <span data-ttu-id="e2eab-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e2eab-119">None</span></span>
<span data-ttu-id="e2eab-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e2eab-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2eab-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2eab-121">OUTPUTS</span></span>

### <span data-ttu-id="e2eab-122">Liste<Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="e2eab-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="e2eab-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2eab-123">NOTES</span></span>

## <span data-ttu-id="e2eab-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2eab-124">RELATED LINKS</span></span>

[<span data-ttu-id="e2eab-125">Add-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="e2eab-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="e2eab-126">Remove-Azanahtarvaultcertificatecontact</span><span class="sxs-lookup"><span data-stu-id="e2eab-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

