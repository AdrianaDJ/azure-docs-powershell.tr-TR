---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24108a767ec1e423d544fa4fb3eaf8bc419f62d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761732"
---
# <span data-ttu-id="a4810-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="a4810-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="a4810-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4810-102">SYNOPSIS</span></span>
<span data-ttu-id="a4810-103">Kullanıcı aboneliklerinin temsil ettiği sağlayıcı teklifleri arasında taşınıp aktarıabileceğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a4810-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="a4810-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4810-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="a4810-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4810-105">DESCRIPTION</span></span>
<span data-ttu-id="a4810-106">Kullanıcı aboneliklerinin temsil ettiği sağlayıcı teklifleri arasında taşınıp aktarıabileceğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a4810-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="a4810-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4810-107">EXAMPLES</span></span>

### <span data-ttu-id="a4810-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4810-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="a4810-109">Test-MoveSubscription \` -destinationdelegatevseçproviderteklifini "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-RESOURCEID "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4E73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="a4810-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="a4810-110">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4810-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="a4810-111">$resourceIds = Get-AzsUserSubscription-Filter "offerName EQ ' O1 '" | Select-ExpandProperty ID Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="a4810-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="a4810-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4810-112">PARAMETERS</span></span>

### <span data-ttu-id="a4810-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a4810-113">-AsJob</span></span>
<span data-ttu-id="a4810-114">Taşıma işleminin iş olarak yürütülüp yürütülmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4810-114">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="a4810-115">-Destinationdelegatevseçproviderteklifini</span><span class="sxs-lookup"><span data-stu-id="a4810-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="a4810-116">Bu cmdlet 'in abonelikleri taşıdıkları tam nitelikli sağlayıcı teklifini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4810-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="a4810-117">Abonelikler varsayılan sağlayıcıya geri taşındıysa NULL.</span><span class="sxs-lookup"><span data-stu-id="a4810-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="a4810-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a4810-118">-ResourceId</span></span>
<span data-ttu-id="a4810-119">Bu cmdlet 'in hareket ettiği tam bir abonelik kaynak tanımlayıcılarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4810-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="a4810-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4810-120">CommonParameters</span></span>
<span data-ttu-id="a4810-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4810-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4810-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4810-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4810-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4810-123">INPUTS</span></span>

## <span data-ttu-id="a4810-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4810-124">OUTPUTS</span></span>

## <span data-ttu-id="a4810-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4810-125">NOTES</span></span>

## <span data-ttu-id="a4810-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4810-126">RELATED LINKS</span></span>

