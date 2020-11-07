---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f415da1d6f9bb086d796c0c1bf191282c2880a09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932188"
---
# <span data-ttu-id="54d62-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="54d62-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="54d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d62-102">SYNOPSIS</span></span>
<span data-ttu-id="54d62-103">Abonelikleri temsilci sağlayıcı teklifleri arasında taşıyın.</span><span class="sxs-lookup"><span data-stu-id="54d62-103">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="54d62-104">Bu süreç yalnızca bir yeniden markalama işlemi yapacak, temeldeki teklif, planlar, aboneliklerin kotaları değiştirilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="54d62-104">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="54d62-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54d62-105">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="54d62-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="54d62-106">DESCRIPTION</span></span>
<span data-ttu-id="54d62-107">Abonelikleri temsilci sağlayıcı teklifleri arasında taşıyın.</span><span class="sxs-lookup"><span data-stu-id="54d62-107">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="54d62-108">Bu süreç yalnızca bir yeniden markalama işlemi yapacak, temeldeki teklif, planlar, aboneliklerin kotaları değiştirilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="54d62-108">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="54d62-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54d62-109">EXAMPLES</span></span>

### <span data-ttu-id="54d62-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="54d62-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="54d62-111">Move-AzsSubscription \` -destinationdelegatevseçproviderteklifini "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-RESOURCEID "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4E73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="54d62-111">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="54d62-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="54d62-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="54d62-113">$resourceIds = Get-AzsUserSubscription-Filter "offerName EQ ' O1 '" | WHERE {$ _. Delegatevseçprovidersubscriptionıd-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select-ExpandProperty ID Move-AzsSubscription-RESOURCEID $resourceIds</span><span class="sxs-lookup"><span data-stu-id="54d62-113">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="54d62-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54d62-114">PARAMETERS</span></span>

### <span data-ttu-id="54d62-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="54d62-115">-AsJob</span></span>
<span data-ttu-id="54d62-116">Taşıma işleminin iş olarak yürütülüp yürütülmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54d62-116">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d62-117">-Destinationdelegatevseçproviderteklifini</span><span class="sxs-lookup"><span data-stu-id="54d62-117">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="54d62-118">Bu cmdlet 'in abonelikleri taşıdıkları tam nitelikli sağlayıcı teklifini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54d62-118">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="54d62-119">Abonelikler varsayılan sağlayıcıya geri taşındıysa NULL.</span><span class="sxs-lookup"><span data-stu-id="54d62-119">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d62-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="54d62-120">-ResourceId</span></span>
<span data-ttu-id="54d62-121">Bu cmdlet 'in hareket ettiği tam bir abonelik kaynak tanımlayıcılarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54d62-121">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d62-122">CommonParameters</span></span>
<span data-ttu-id="54d62-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54d62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d62-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d62-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d62-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54d62-125">INPUTS</span></span>

## <span data-ttu-id="54d62-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54d62-126">OUTPUTS</span></span>

## <span data-ttu-id="54d62-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54d62-127">NOTES</span></span>

## <span data-ttu-id="54d62-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54d62-128">RELATED LINKS</span></span>

