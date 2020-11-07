---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764060"
---
# <span data-ttu-id="a9d15-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a9d15-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a9d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9d15-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d15-103">Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="a9d15-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9d15-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9d15-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9d15-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d15-106">**Get-AzureKeyVaultCertificateContact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="a9d15-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a9d15-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9d15-107">EXAMPLES</span></span>

### <span data-ttu-id="a9d15-108">Örnek 1: tüm sertifika kişilerini alma</span><span class="sxs-lookup"><span data-stu-id="a9d15-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="a9d15-109">Bu komut contoso tuş Kasası 'ndaki sertifika nesneleri için tüm kişileri alır ve $Contacts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a9d15-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="a9d15-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9d15-110">PARAMETERS</span></span>

### <span data-ttu-id="a9d15-111">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a9d15-111">-VaultName</span></span>
<span data-ttu-id="a9d15-112">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9d15-112">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="a9d15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d15-113">-DefaultProfile</span></span>
<span data-ttu-id="a9d15-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9d15-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9d15-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d15-115">CommonParameters</span></span>
<span data-ttu-id="a9d15-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9d15-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d15-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d15-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d15-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9d15-118">INPUTS</span></span>

## <span data-ttu-id="a9d15-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9d15-119">OUTPUTS</span></span>

### <span data-ttu-id="a9d15-120">Liste<Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="a9d15-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="a9d15-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9d15-121">NOTES</span></span>

## <span data-ttu-id="a9d15-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9d15-122">RELATED LINKS</span></span>

[<span data-ttu-id="a9d15-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a9d15-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="a9d15-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a9d15-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

