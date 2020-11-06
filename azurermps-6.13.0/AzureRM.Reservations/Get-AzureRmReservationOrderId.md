---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: 1e60ca2ce1a845fa460e14a4e99b921fa4c085ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588390"
---
# <span data-ttu-id="b2b0a-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="b2b0a-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="b2b0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b0a-103">Uygun kimlikler listesini alın `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="b2b0a-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2b0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2b0a-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2b0a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2b0a-105">DESCRIPTION</span></span>
<span data-ttu-id="b2b0a-106">`ReservationOrder`Bu aboneliğe uygulanabilecek geçerli s kimliklerini alın.</span><span class="sxs-lookup"><span data-stu-id="b2b0a-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="b2b0a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2b0a-107">EXAMPLES</span></span>

### <span data-ttu-id="b2b0a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b2b0a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="b2b0a-109">`ReservationOrder`Varsayılan aboneliğe uygulanır</span><span class="sxs-lookup"><span data-stu-id="b2b0a-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="b2b0a-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b2b0a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="b2b0a-111">`ReservationOrder`Belirtilen aboneliğe uygulanır</span><span class="sxs-lookup"><span data-stu-id="b2b0a-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="b2b0a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2b0a-112">PARAMETERS</span></span>

### <span data-ttu-id="b2b0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b0a-113">-DefaultProfile</span></span>
<span data-ttu-id="b2b0a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2b0a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2b0a-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b2b0a-115">-SubscriptionId</span></span>
<span data-ttu-id="b2b0a-116">Uygulanacak s aboneliğinin kimliği `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="b2b0a-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b0a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b0a-117">CommonParameters</span></span>
<span data-ttu-id="b2b0a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2b0a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b0a-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b0a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b0a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2b0a-120">INPUTS</span></span>

### <span data-ttu-id="b2b0a-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b2b0a-121">None</span></span>

## <span data-ttu-id="b2b0a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2b0a-122">OUTPUTS</span></span>

### <span data-ttu-id="b2b0a-123">Microsoft. Azure. Management. rezervasyonlar. modeller. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="b2b0a-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="b2b0a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2b0a-124">NOTES</span></span>

## <span data-ttu-id="b2b0a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2b0a-125">RELATED LINKS</span></span>
