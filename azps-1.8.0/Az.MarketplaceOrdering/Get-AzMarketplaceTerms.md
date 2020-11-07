---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 22a9c9b11063dfd9a84e8ecf292af6e9e0f7f97f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915780"
---
# <span data-ttu-id="ab69a-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ab69a-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="ab69a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab69a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab69a-103">Belirli bir yayıncı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için anlaşma şartlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="ab69a-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ab69a-104">Bu komut tarafından döndürülen terimler nesnesinin yasal şartları kabul etmesi için Set-AzMarketplaceTerms geçirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab69a-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="ab69a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab69a-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab69a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab69a-106">DESCRIPTION</span></span>
<span data-ttu-id="ab69a-107">**Get-AzMarketplaceTerms** cmdlet 'i, verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan No (ad) başlığı için şartlar döndürür.</span><span class="sxs-lookup"><span data-stu-id="ab69a-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="ab69a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab69a-108">EXAMPLES</span></span>

### <span data-ttu-id="ab69a-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ab69a-109">Example 1</span></span>
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

## <span data-ttu-id="ab69a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab69a-110">PARAMETERS</span></span>

### <span data-ttu-id="ab69a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab69a-111">-DefaultProfile</span></span>
<span data-ttu-id="ab69a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab69a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab69a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab69a-113">-Name</span></span>
<span data-ttu-id="ab69a-114">Dağıtılan resmin tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="ab69a-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ab69a-115">-Ürün</span><span class="sxs-lookup"><span data-stu-id="ab69a-115">-Product</span></span>
<span data-ttu-id="ab69a-116">Dağıtılan resmin teklif tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="ab69a-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ab69a-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ab69a-117">-Publisher</span></span>
<span data-ttu-id="ab69a-118">Dağıtılan resmin yayımcı tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="ab69a-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ab69a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab69a-119">CommonParameters</span></span>
<span data-ttu-id="ab69a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab69a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab69a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab69a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab69a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab69a-122">INPUTS</span></span>

### <span data-ttu-id="ab69a-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ab69a-123">None</span></span>

## <span data-ttu-id="ab69a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab69a-124">OUTPUTS</span></span>

### <span data-ttu-id="ab69a-125">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="ab69a-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="ab69a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab69a-126">NOTES</span></span>

## <span data-ttu-id="ab69a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab69a-127">RELATED LINKS</span></span>
