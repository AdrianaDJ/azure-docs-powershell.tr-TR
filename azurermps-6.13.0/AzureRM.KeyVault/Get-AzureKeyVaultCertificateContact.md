---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763853"
---
# <span data-ttu-id="05710-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="05710-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="05710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05710-102">SYNOPSIS</span></span>
<span data-ttu-id="05710-103">Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="05710-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05710-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05710-104">SYNTAX</span></span>

### <span data-ttu-id="05710-105">VaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05710-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05710-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05710-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05710-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="05710-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05710-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="05710-108">DESCRIPTION</span></span>
<span data-ttu-id="05710-109">**Get-AzureKeyVaultCertificateContact** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir Anahtar Kasası için sertifika bildirimleri için kaydedilmiş kişileri alır.</span><span class="sxs-lookup"><span data-stu-id="05710-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="05710-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05710-110">EXAMPLES</span></span>

### <span data-ttu-id="05710-111">Örnek 1: tüm sertifika kişilerini alma</span><span class="sxs-lookup"><span data-stu-id="05710-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="05710-112">Bu komut contoso tuş Kasası 'ndaki sertifika nesneleri için tüm kişileri alır ve $Contacts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="05710-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="05710-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05710-113">PARAMETERS</span></span>

### <span data-ttu-id="05710-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05710-114">-DefaultProfile</span></span>
<span data-ttu-id="05710-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="05710-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05710-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05710-116">-InputObject</span></span>
<span data-ttu-id="05710-117">Tuş Kasası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="05710-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05710-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="05710-118">-ResourceId</span></span>
<span data-ttu-id="05710-119">Tuş Kasası kimliği.</span><span class="sxs-lookup"><span data-stu-id="05710-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="05710-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="05710-120">-VaultName</span></span>
<span data-ttu-id="05710-121">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05710-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05710-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05710-122">CommonParameters</span></span>
<span data-ttu-id="05710-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05710-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05710-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05710-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05710-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05710-125">INPUTS</span></span>

### <span data-ttu-id="05710-126">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="05710-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="05710-127">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="05710-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="05710-128">System. String</span><span class="sxs-lookup"><span data-stu-id="05710-128">System.String</span></span>

## <span data-ttu-id="05710-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05710-129">OUTPUTS</span></span>

### <span data-ttu-id="05710-130">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="05710-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="05710-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05710-131">NOTES</span></span>

## <span data-ttu-id="05710-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05710-132">RELATED LINKS</span></span>

[<span data-ttu-id="05710-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="05710-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="05710-134">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="05710-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

