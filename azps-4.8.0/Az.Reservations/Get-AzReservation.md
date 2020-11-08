---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274688"
---
# <span data-ttu-id="dd47f-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="dd47f-101">Get-AzReservation</span></span>

## <span data-ttu-id="dd47f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd47f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd47f-103">`Reservation`Belirli bir ayırma emrinde s alın</span><span class="sxs-lookup"><span data-stu-id="dd47f-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="dd47f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd47f-104">SYNTAX</span></span>

### <span data-ttu-id="dd47f-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd47f-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd47f-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="dd47f-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd47f-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="dd47f-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd47f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd47f-108">DESCRIPTION</span></span>
<span data-ttu-id="dd47f-109">`Reservation`Tek bir `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="dd47f-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="dd47f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd47f-110">EXAMPLES</span></span>

### <span data-ttu-id="dd47f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd47f-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="dd47f-112">`Reservation`Belirtilen içinde liste s `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="dd47f-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="dd47f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dd47f-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="dd47f-114">Belirli `Reservation` Ayrıntılar edinin.</span><span class="sxs-lookup"><span data-stu-id="dd47f-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="dd47f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd47f-115">PARAMETERS</span></span>

### <span data-ttu-id="dd47f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd47f-116">-DefaultProfile</span></span>
<span data-ttu-id="dd47f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd47f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd47f-118">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="dd47f-118">-ReservationId</span></span>
<span data-ttu-id="dd47f-119">`Reservation`Bakılacak yer</span><span class="sxs-lookup"><span data-stu-id="dd47f-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd47f-120">-Rezervde</span><span class="sxs-lookup"><span data-stu-id="dd47f-120">-ReservationOrder</span></span>
<span data-ttu-id="dd47f-121">İçin yöneltme nesnesi parametresi `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="dd47f-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd47f-122">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="dd47f-122">-ReservationOrderId</span></span>
<span data-ttu-id="dd47f-123">`ReservationOrder`, `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="dd47f-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="dd47f-124">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="dd47f-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd47f-125">-Rezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="dd47f-125">-ReservationOrderPage</span></span>
<span data-ttu-id="dd47f-126">İçin yöneltme nesnesi parametresi `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="dd47f-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd47f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd47f-127">CommonParameters</span></span>
<span data-ttu-id="dd47f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd47f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd47f-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dd47f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd47f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd47f-130">INPUTS</span></span>

### <span data-ttu-id="dd47f-131">System. Guid</span><span class="sxs-lookup"><span data-stu-id="dd47f-131">System.Guid</span></span>

### <span data-ttu-id="dd47f-132">Microsoft. Azure. Commands. rezervasyonlar. model. psrezerv</span><span class="sxs-lookup"><span data-stu-id="dd47f-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="dd47f-133">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="dd47f-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="dd47f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd47f-134">OUTPUTS</span></span>

### <span data-ttu-id="dd47f-135">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationpage</span><span class="sxs-lookup"><span data-stu-id="dd47f-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="dd47f-136">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="dd47f-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="dd47f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd47f-137">NOTES</span></span>

## <span data-ttu-id="dd47f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd47f-138">RELATED LINKS</span></span>
