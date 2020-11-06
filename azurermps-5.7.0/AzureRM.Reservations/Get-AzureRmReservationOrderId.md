---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589697"
---
# <span data-ttu-id="6aa4a-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6aa4a-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="6aa4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa4a-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa4a-103">Uygun kimlikler listesini alın `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="6aa4a-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aa4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6aa4a-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="6aa4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6aa4a-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa4a-106">`ReservationOrder`Bu aboneliğe uygulanabilecek geçerli s kimliklerini alın.</span><span class="sxs-lookup"><span data-stu-id="6aa4a-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="6aa4a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6aa4a-107">EXAMPLES</span></span>

### <span data-ttu-id="6aa4a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6aa4a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="6aa4a-109">`ReservationOrder`Varsayılan aboneliğe uygulanır</span><span class="sxs-lookup"><span data-stu-id="6aa4a-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="6aa4a-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6aa4a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="6aa4a-111">`ReservationOrder`Belirtilen aboneliğe uygulanır</span><span class="sxs-lookup"><span data-stu-id="6aa4a-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="6aa4a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6aa4a-112">PARAMETERS</span></span>

### <span data-ttu-id="6aa4a-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6aa4a-113">-SubscriptionId</span></span>
<span data-ttu-id="6aa4a-114">Uygulanacak s aboneliğinin kimliği `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="6aa4a-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa4a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa4a-115">CommonParameters</span></span>
<span data-ttu-id="6aa4a-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6aa4a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa4a-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa4a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa4a-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6aa4a-118">INPUTS</span></span>

### <span data-ttu-id="6aa4a-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6aa4a-119">None</span></span>

## <span data-ttu-id="6aa4a-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6aa4a-120">OUTPUTS</span></span>

### <span data-ttu-id="6aa4a-121">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psappliedrezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="6aa4a-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="6aa4a-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6aa4a-122">NOTES</span></span>

## <span data-ttu-id="6aa4a-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6aa4a-123">RELATED LINKS</span></span>

