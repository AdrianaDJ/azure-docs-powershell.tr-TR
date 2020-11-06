---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 29f3d645791dfa0b4f70ed936ccfcb4f72671038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594642"
---
# <span data-ttu-id="f5e53-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="f5e53-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="f5e53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e53-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e53-103">Belirli bir yayıncı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için anlaşma şartlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="f5e53-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="f5e53-104">Bu komut tarafından döndürülen terimler nesnesinin yasal şartları kabul etmesi için Set-AzureRmMarketplaceTerms geçirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f5e53-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5e53-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5e53-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5e53-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5e53-106">DESCRIPTION</span></span>
<span data-ttu-id="f5e53-107">**Get-AzureRmMarketplaceTerms** cmdlet 'i, verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan No (ad) tanımlama terimlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f5e53-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="f5e53-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5e53-108">EXAMPLES</span></span>

### <span data-ttu-id="f5e53-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f5e53-109">Example 1</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="f5e53-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5e53-110">PARAMETERS</span></span>

### <span data-ttu-id="f5e53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e53-111">-DefaultProfile</span></span>
<span data-ttu-id="f5e53-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5e53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5e53-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5e53-113">-Name</span></span>
<span data-ttu-id="f5e53-114">Dağıtılan resmin tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="f5e53-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e53-115">-Ürün</span><span class="sxs-lookup"><span data-stu-id="f5e53-115">-Product</span></span>
<span data-ttu-id="f5e53-116">Dağıtılan resmin teklif tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="f5e53-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e53-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f5e53-117">-Publisher</span></span>
<span data-ttu-id="f5e53-118">Dağıtılan resmin yayımcı tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="f5e53-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e53-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e53-119">CommonParameters</span></span>
<span data-ttu-id="f5e53-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5e53-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e53-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e53-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e53-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5e53-122">INPUTS</span></span>

### <span data-ttu-id="f5e53-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f5e53-123">None</span></span>

## <span data-ttu-id="f5e53-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5e53-124">OUTPUTS</span></span>

### <span data-ttu-id="f5e53-125">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="f5e53-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="f5e53-126">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="f5e53-126">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="f5e53-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5e53-127">NOTES</span></span>

## <span data-ttu-id="f5e53-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5e53-128">RELATED LINKS</span></span>

