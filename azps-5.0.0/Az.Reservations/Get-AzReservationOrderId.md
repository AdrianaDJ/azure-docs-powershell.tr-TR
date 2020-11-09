---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322154"
---
# <span data-ttu-id="57616-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="57616-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="57616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57616-102">SYNOPSIS</span></span>
<span data-ttu-id="57616-103">Uygun kimlikler listesini alın `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="57616-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="57616-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57616-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57616-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57616-105">DESCRIPTION</span></span>
<span data-ttu-id="57616-106">`ReservationOrder`Bu aboneliğe uygulanabilecek geçerli s kimliklerini alın.</span><span class="sxs-lookup"><span data-stu-id="57616-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="57616-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57616-107">EXAMPLES</span></span>

### <span data-ttu-id="57616-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="57616-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="57616-109">`ReservationOrder`Varsayılan aboneliğe uygulanır</span><span class="sxs-lookup"><span data-stu-id="57616-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="57616-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="57616-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="57616-111">`ReservationOrder`Belirtilen aboneliğe uygulanır</span><span class="sxs-lookup"><span data-stu-id="57616-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="57616-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57616-112">PARAMETERS</span></span>

### <span data-ttu-id="57616-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57616-113">-DefaultProfile</span></span>
<span data-ttu-id="57616-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57616-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57616-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="57616-115">-SubscriptionId</span></span>
<span data-ttu-id="57616-116">Uygulanacak s aboneliğinin kimliği `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="57616-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="57616-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57616-117">CommonParameters</span></span>
<span data-ttu-id="57616-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57616-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57616-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="57616-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57616-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57616-120">INPUTS</span></span>

### <span data-ttu-id="57616-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="57616-121">None</span></span>

## <span data-ttu-id="57616-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57616-122">OUTPUTS</span></span>

### <span data-ttu-id="57616-123">Microsoft. Azure. Management. rezervasyonlar. modeller. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="57616-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="57616-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57616-124">NOTES</span></span>

## <span data-ttu-id="57616-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57616-125">RELATED LINKS</span></span>
