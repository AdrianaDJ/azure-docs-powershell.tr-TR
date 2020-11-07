---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938132"
---
# <span data-ttu-id="0f486-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="0f486-101">Get-AzReservation</span></span>

## <span data-ttu-id="0f486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f486-102">SYNOPSIS</span></span>
<span data-ttu-id="0f486-103">`Reservation`Belirli bir ayırma emrinde s alın</span><span class="sxs-lookup"><span data-stu-id="0f486-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="0f486-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f486-104">SYNTAX</span></span>

### <span data-ttu-id="0f486-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f486-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f486-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="0f486-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f486-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="0f486-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f486-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f486-108">DESCRIPTION</span></span>
<span data-ttu-id="0f486-109">`Reservation`Tek bir `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="0f486-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="0f486-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f486-110">EXAMPLES</span></span>

### <span data-ttu-id="0f486-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0f486-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="0f486-112">`Reservation`Belirtilen içinde liste s `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="0f486-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="0f486-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0f486-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="0f486-114">Belirli `Reservation` Ayrıntılar edinin.</span><span class="sxs-lookup"><span data-stu-id="0f486-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="0f486-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f486-115">PARAMETERS</span></span>

### <span data-ttu-id="0f486-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f486-116">-DefaultProfile</span></span>
<span data-ttu-id="0f486-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f486-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f486-118">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="0f486-118">-ReservationId</span></span>
<span data-ttu-id="0f486-119">`Reservation`Bakılacak yer</span><span class="sxs-lookup"><span data-stu-id="0f486-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="0f486-120">-Rezervde</span><span class="sxs-lookup"><span data-stu-id="0f486-120">-ReservationOrder</span></span>
<span data-ttu-id="0f486-121">İçin yöneltme nesnesi parametresi `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="0f486-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="0f486-122">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="0f486-122">-ReservationOrderId</span></span>
<span data-ttu-id="0f486-123">`ReservationOrder`, `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="0f486-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="0f486-124">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="0f486-124">Required.</span></span>

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

### <span data-ttu-id="0f486-125">-Rezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="0f486-125">-ReservationOrderPage</span></span>
<span data-ttu-id="0f486-126">İçin yöneltme nesnesi parametresi `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="0f486-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="0f486-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f486-127">CommonParameters</span></span>
<span data-ttu-id="0f486-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f486-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f486-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0f486-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f486-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f486-130">INPUTS</span></span>

### <span data-ttu-id="0f486-131">System. Guid</span><span class="sxs-lookup"><span data-stu-id="0f486-131">System.Guid</span></span>

### <span data-ttu-id="0f486-132">Microsoft. Azure. Commands. rezervasyonlar. model. psrezerv</span><span class="sxs-lookup"><span data-stu-id="0f486-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="0f486-133">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="0f486-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="0f486-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f486-134">OUTPUTS</span></span>

### <span data-ttu-id="0f486-135">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationpage</span><span class="sxs-lookup"><span data-stu-id="0f486-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="0f486-136">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="0f486-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="0f486-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f486-137">NOTES</span></span>

## <span data-ttu-id="0f486-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f486-138">RELATED LINKS</span></span>
