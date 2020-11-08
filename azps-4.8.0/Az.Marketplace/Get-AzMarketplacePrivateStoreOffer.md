---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109952"
---
# <span data-ttu-id="62b0e-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="62b0e-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="62b0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="62b0e-103">Bir veya daha fazla özel mağazanın teklifini edinin.</span><span class="sxs-lookup"><span data-stu-id="62b0e-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="62b0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62b0e-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62b0e-105">DESCRIPTION</span></span>
<span data-ttu-id="62b0e-106">Kiracı kapsamı altında eklenmiş olan ortak + özel planlar içeren bir veya daha fazla özel mağazanın teklifini edinin.</span><span class="sxs-lookup"><span data-stu-id="62b0e-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="62b0e-107">Abonelik kimliği temsil ediyorsanız, özel planlar içeren bir veya daha fazla özel mağazanın teklifini yalnızca abonelik kapsamında alın</span><span class="sxs-lookup"><span data-stu-id="62b0e-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="62b0e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62b0e-108">EXAMPLES</span></span>

### <span data-ttu-id="62b0e-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="62b0e-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="62b0e-110">Özel mağazanın, kiracı kapsamı altına eklenmiş özel + genel planlarla teklifleri alın.</span><span class="sxs-lookup"><span data-stu-id="62b0e-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="62b0e-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="62b0e-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="62b0e-112">Özel mağazalardan yalnızca abonelik kapsamı altına eklenen özel planlar alın.</span><span class="sxs-lookup"><span data-stu-id="62b0e-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="62b0e-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="62b0e-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="62b0e-114">Özel mağazanın teklifini kiracı kapsamı altına eklenmiş özel + genel planlarıyla edinin.</span><span class="sxs-lookup"><span data-stu-id="62b0e-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="62b0e-115">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="62b0e-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="62b0e-116">Özel mağazalardan yalnızca kiracı kapsamı altında eklenmiş olan özel planlar alın.</span><span class="sxs-lookup"><span data-stu-id="62b0e-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="62b0e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62b0e-117">PARAMETERS</span></span>

### <span data-ttu-id="62b0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b0e-118">-DefaultProfile</span></span>
<span data-ttu-id="62b0e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62b0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b0e-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="62b0e-120">-OfferId</span></span>
<span data-ttu-id="62b0e-121">Gerekli Azure Market privateStore teklifi</span><span class="sxs-lookup"><span data-stu-id="62b0e-121">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b0e-122">-Privatestoreıd</span><span class="sxs-lookup"><span data-stu-id="62b0e-122">-PrivateStoreId</span></span>
<span data-ttu-id="62b0e-123">Gerekli Azure Market privateStore teklifleri</span><span class="sxs-lookup"><span data-stu-id="62b0e-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="62b0e-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="62b0e-124">-SubscriptionId</span></span>
<span data-ttu-id="62b0e-125">Azure Market aboneliği kimliği</span><span class="sxs-lookup"><span data-stu-id="62b0e-125">Azure Marketplace subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b0e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b0e-126">CommonParameters</span></span>
<span data-ttu-id="62b0e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62b0e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b0e-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62b0e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b0e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62b0e-129">INPUTS</span></span>

### <span data-ttu-id="62b0e-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="62b0e-130">None</span></span>

## <span data-ttu-id="62b0e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62b0e-131">OUTPUTS</span></span>

### <span data-ttu-id="62b0e-132">Microsoft. Azure. Commands. Market. model. PrivateStore. Psprivatestoreteklifini</span><span class="sxs-lookup"><span data-stu-id="62b0e-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="62b0e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62b0e-133">NOTES</span></span>

## <span data-ttu-id="62b0e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62b0e-134">RELATED LINKS</span></span>
