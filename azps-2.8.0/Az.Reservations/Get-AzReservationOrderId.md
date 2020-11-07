---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: c969d24a894165e23628b91cda640f676ec3f3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933382"
---
# <span data-ttu-id="344aa-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="344aa-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="344aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="344aa-102">SYNOPSIS</span></span>
<span data-ttu-id="344aa-103">Uygun kimlikler listesini alın `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="344aa-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="344aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="344aa-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="344aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="344aa-105">DESCRIPTION</span></span>
<span data-ttu-id="344aa-106">`ReservationOrder`Bu aboneliğe uygulanabilecek geçerli s kimliklerini alın.</span><span class="sxs-lookup"><span data-stu-id="344aa-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="344aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="344aa-107">EXAMPLES</span></span>

### <span data-ttu-id="344aa-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="344aa-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="344aa-109">`ReservationOrder`Varsayılan aboneliğe uygulanır</span><span class="sxs-lookup"><span data-stu-id="344aa-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="344aa-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="344aa-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="344aa-111">`ReservationOrder`Belirtilen aboneliğe uygulanır</span><span class="sxs-lookup"><span data-stu-id="344aa-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="344aa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="344aa-112">PARAMETERS</span></span>

### <span data-ttu-id="344aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344aa-113">-DefaultProfile</span></span>
<span data-ttu-id="344aa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="344aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="344aa-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="344aa-115">-SubscriptionId</span></span>
<span data-ttu-id="344aa-116">Uygulanacak s aboneliğinin kimliği `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="344aa-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="344aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344aa-117">CommonParameters</span></span>
<span data-ttu-id="344aa-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="344aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344aa-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="344aa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344aa-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="344aa-120">INPUTS</span></span>

### <span data-ttu-id="344aa-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="344aa-121">None</span></span>

## <span data-ttu-id="344aa-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="344aa-122">OUTPUTS</span></span>

### <span data-ttu-id="344aa-123">Microsoft. Azure. Management. rezervasyonlar. modeller. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="344aa-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="344aa-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="344aa-124">NOTES</span></span>

## <span data-ttu-id="344aa-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="344aa-125">RELATED LINKS</span></span>
