---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268996"
---
# <span data-ttu-id="9365f-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="9365f-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="9365f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9365f-102">SYNOPSIS</span></span>
<span data-ttu-id="9365f-103">Belirli bir yayıncı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için anlaşma şartlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="9365f-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="9365f-104">Bu komut tarafından döndürülen terimler nesnesinin yasal şartları kabul etmesi için Set-AzMarketplaceTerms geçirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9365f-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="9365f-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9365f-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9365f-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9365f-106">DESCRIPTION</span></span>
<span data-ttu-id="9365f-107">**Get-AzMarketplaceTerms** cmdlet 'i, verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan No (ad) başlığı için şartlar döndürür.</span><span class="sxs-lookup"><span data-stu-id="9365f-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="9365f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9365f-108">EXAMPLES</span></span>

### <span data-ttu-id="9365f-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9365f-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="9365f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9365f-110">PARAMETERS</span></span>

### <span data-ttu-id="9365f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9365f-111">-DefaultProfile</span></span>
<span data-ttu-id="9365f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9365f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9365f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9365f-113">-Name</span></span>
<span data-ttu-id="9365f-114">Dağıtılan resmin tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="9365f-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9365f-115">-Ürün</span><span class="sxs-lookup"><span data-stu-id="9365f-115">-Product</span></span>
<span data-ttu-id="9365f-116">Dağıtılan resmin teklif tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="9365f-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9365f-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9365f-117">-Publisher</span></span>
<span data-ttu-id="9365f-118">Dağıtılan resmin yayımcı tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="9365f-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9365f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9365f-119">CommonParameters</span></span>
<span data-ttu-id="9365f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9365f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9365f-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9365f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9365f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9365f-122">INPUTS</span></span>

### <span data-ttu-id="9365f-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9365f-123">None</span></span>

## <span data-ttu-id="9365f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9365f-124">OUTPUTS</span></span>

### <span data-ttu-id="9365f-125">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="9365f-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="9365f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9365f-126">NOTES</span></span>

## <span data-ttu-id="9365f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9365f-127">RELATED LINKS</span></span>
