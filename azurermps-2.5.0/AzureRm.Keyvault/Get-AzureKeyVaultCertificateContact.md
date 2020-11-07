---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: d6d2070afcb4a5b9b0b13af1fa54dc93621c5a97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939370"
---
# <span data-ttu-id="8fa6d-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8fa6d-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8fa6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fa6d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa6d-103">Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="8fa6d-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fa6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fa6d-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fa6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fa6d-105">DESCRIPTION</span></span>
<span data-ttu-id="8fa6d-106">**Get-AzureKeyVaultCertificateContact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="8fa6d-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="8fa6d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fa6d-107">EXAMPLES</span></span>

### <span data-ttu-id="8fa6d-108">Örnek 1: tüm sertifika kişilerini alma</span><span class="sxs-lookup"><span data-stu-id="8fa6d-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="8fa6d-109">Bu komut contoso tuş Kasası 'ndaki sertifika nesneleri için tüm kişileri alır ve $Contacts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8fa6d-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="8fa6d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fa6d-110">PARAMETERS</span></span>

### <span data-ttu-id="8fa6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa6d-111">-DefaultProfile</span></span>
<span data-ttu-id="8fa6d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8fa6d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fa6d-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8fa6d-113">-VaultName</span></span>
<span data-ttu-id="8fa6d-114">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fa6d-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="8fa6d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa6d-115">CommonParameters</span></span>
<span data-ttu-id="8fa6d-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fa6d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa6d-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa6d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa6d-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fa6d-118">INPUTS</span></span>

## <span data-ttu-id="8fa6d-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fa6d-119">OUTPUTS</span></span>

### <span data-ttu-id="8fa6d-120">Liste<Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="8fa6d-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="8fa6d-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fa6d-121">NOTES</span></span>

## <span data-ttu-id="8fa6d-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fa6d-122">RELATED LINKS</span></span>

[<span data-ttu-id="8fa6d-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8fa6d-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="8fa6d-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8fa6d-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

