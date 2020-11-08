---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268993"
---
# <span data-ttu-id="9facb-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="9facb-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="9facb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9facb-102">SYNOPSIS</span></span>
<span data-ttu-id="9facb-103">Özel depolama için teklif güncelleştirir veya oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9facb-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="9facb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9facb-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9facb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9facb-105">DESCRIPTION</span></span>
<span data-ttu-id="9facb-106">Kiracı kapsamı altında oluşturulmuş özel mağaza için bu teklifi güncelleştirir veya oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9facb-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="9facb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9facb-107">EXAMPLES</span></span>

### <span data-ttu-id="9facb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9facb-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="9facb-109">Kiracı kapsamı altında oluşturulmuş özel mağaza için özel + genel planlar içeren teklif oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9facb-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="9facb-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9facb-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="9facb-111">Yalnızca abonelik kapsamı altında oluşturulan özel mağaza için özel planlar içeren teklif oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9facb-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="9facb-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9facb-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="9facb-113">Güncelleştirmeler, kiracı kapsamı altında oluşturulmuş özel mağaza için özel + genel planlarıyla birlikte sunulur.</span><span class="sxs-lookup"><span data-stu-id="9facb-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="9facb-114">ETag gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9facb-114">Etag is needed.</span></span>

### <span data-ttu-id="9facb-115">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="9facb-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="9facb-116">Güncelleştirmeler yalnızca abonelik kapsamı altında oluşturulan özel planlarla özel mağaza için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="9facb-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="9facb-117">ETag gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9facb-117">Etag is needed.</span></span>


## <span data-ttu-id="9facb-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9facb-118">PARAMETERS</span></span>

### <span data-ttu-id="9facb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9facb-119">-DefaultProfile</span></span>
<span data-ttu-id="9facb-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9facb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9facb-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="9facb-121">-ETag</span></span>
<span data-ttu-id="9facb-122">Azure Market privateStore 'ın güncelleştirme için eTag 'i</span><span class="sxs-lookup"><span data-stu-id="9facb-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="9facb-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="9facb-123">-OfferId</span></span>
<span data-ttu-id="9facb-124">Gerekli Azure Market privateStore teklifi</span><span class="sxs-lookup"><span data-stu-id="9facb-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="9facb-125">-Privatestoreıd</span><span class="sxs-lookup"><span data-stu-id="9facb-125">-PrivateStoreId</span></span>
<span data-ttu-id="9facb-126">Gerekli Azure Market privateStore teklifleri</span><span class="sxs-lookup"><span data-stu-id="9facb-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="9facb-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="9facb-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="9facb-128">Gerekli Azure Market privateStore teklifinin belirli plan kimlikleri sınırlaması</span><span class="sxs-lookup"><span data-stu-id="9facb-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9facb-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="9facb-129">-Confirm</span></span>
<span data-ttu-id="9facb-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9facb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9facb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9facb-131">-WhatIf</span></span>
<span data-ttu-id="9facb-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9facb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9facb-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9facb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9facb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9facb-134">CommonParameters</span></span>
<span data-ttu-id="9facb-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9facb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9facb-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9facb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9facb-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9facb-137">INPUTS</span></span>

### <span data-ttu-id="9facb-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9facb-138">None</span></span>

## <span data-ttu-id="9facb-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9facb-139">OUTPUTS</span></span>

### <span data-ttu-id="9facb-140">Microsoft. Azure. Commands. Market. model. PrivateStore. Psprivatestoreteklifini</span><span class="sxs-lookup"><span data-stu-id="9facb-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="9facb-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9facb-141">NOTES</span></span>

## <span data-ttu-id="9facb-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9facb-142">RELATED LINKS</span></span>
