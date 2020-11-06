---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573313"
---
# <span data-ttu-id="999e8-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="999e8-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="999e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="999e8-102">SYNOPSIS</span></span>
<span data-ttu-id="999e8-103">`Reservation`Belirli bir ayırma emrinde s alın</span><span class="sxs-lookup"><span data-stu-id="999e8-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="999e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="999e8-104">SYNTAX</span></span>

### <span data-ttu-id="999e8-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="999e8-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="999e8-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="999e8-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="999e8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="999e8-107">DESCRIPTION</span></span>
<span data-ttu-id="999e8-108">`Reservation`Tek bir `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="999e8-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="999e8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="999e8-109">EXAMPLES</span></span>

### <span data-ttu-id="999e8-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="999e8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="999e8-111">`Reservation`Belirtilen içinde liste s `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="999e8-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="999e8-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="999e8-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="999e8-113">Belirli `Reservation` Ayrıntılar edinin.</span><span class="sxs-lookup"><span data-stu-id="999e8-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="999e8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="999e8-114">PARAMETERS</span></span>

### <span data-ttu-id="999e8-115">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="999e8-115">-ReservationId</span></span>
<span data-ttu-id="999e8-116">`Reservation`Bakılacak yer</span><span class="sxs-lookup"><span data-stu-id="999e8-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999e8-117">-Rezervde</span><span class="sxs-lookup"><span data-stu-id="999e8-117">-ReservationOrder</span></span>
<span data-ttu-id="999e8-118">İçin yöneltme nesnesi parametresi `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="999e8-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="999e8-119">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="999e8-119">-ReservationOrderId</span></span>
<span data-ttu-id="999e8-120">`ReservationOrder`, `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="999e8-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="999e8-121">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="999e8-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999e8-122">-Rezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="999e8-122">-ReservationOrderPage</span></span>
<span data-ttu-id="999e8-123">İçin yöneltme nesnesi parametresi `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="999e8-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="999e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999e8-124">CommonParameters</span></span>
<span data-ttu-id="999e8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="999e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999e8-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="999e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999e8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="999e8-127">INPUTS</span></span>

### <span data-ttu-id="999e8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="999e8-128">System.String</span></span>
<span data-ttu-id="999e8-129">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationorder Microsoft. Azure. Commands. rezervasyonlar. model. Psrezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="999e8-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="999e8-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="999e8-130">OUTPUTS</span></span>

### <span data-ttu-id="999e8-131">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationpage</span><span class="sxs-lookup"><span data-stu-id="999e8-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="999e8-132">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="999e8-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="999e8-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="999e8-133">NOTES</span></span>

## <span data-ttu-id="999e8-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="999e8-134">RELATED LINKS</span></span>

